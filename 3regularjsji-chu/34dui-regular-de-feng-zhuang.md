# 对Regular的封装

工程中最关键的基础组件有BaseComponent、ListComponent和BaseModal；

## BaseComponent

* 路径：src/javascript/widget/BaseComponent.js
* 作用：因为工程中所有组件都是从BaseComponent继承扩展的，所以所有组件通用的方法会放在BaseComponent中；例如request方法，所有页面的请求都可以直接是用this.$request方法请求后端数据，request还做了code非200的统一处理，自己只需要关心调用成功后的处理逻辑；

## ListComponent

* 路径：src/javascript/component/NEKListComponent.js
* 作用：对列表分页、请求数据的封装；需要分页的列表，只需要继承ListComponent，就不需要处理分页相关的数据逻辑；请求数据也可以直接调用this._getList\(\)方法；如果默认的返回结果处理函数\_\_\_bodyResolver不能满足需求，可在子组件内override这个函数；

## BaseModal\(各工程可能路径不同\)

* 路径：src/javascript/component/modal/index.js
* 3种用法：
  * 如果弹框模板只是一句文案，可以直接使用BaseModal的静态方法BaseModal.confirm\(xxx\), BaseModal.alert\(xxx\);
  * 如果模板较复杂，则与ListComponent一样， 继承BaseModal，写自己的模板和逻辑；
  * 如果不仅是一句文案，但模板也比较简单，可以直接
  * ```
    var modal = new BaseModal({
        data: {
            contentTemplate: '<ui.input value="{testValue}" />'
        }
    });
    modal.$on('ok', function() {
        // 处理逻辑
        // 可以通过modal.data.xxx访问到contentTemplate中写的数据
        console.log(modal.data.testValue)
    });
    ```



