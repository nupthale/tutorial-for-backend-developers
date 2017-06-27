# 对Regular的封装

工程中最关键的基础组件有BaseComponent、ListComponent和BaseModal；

## BaseComponent

* 路径：src/javascript/widget/BaseComponent.js
* 作用：因为工程中所有组件都是从BaseComponent继承扩展的，所以所有组件通用的方法会放在BaseComponent中；例如request方法，所有页面的请求都可以直接是用this.$request方法请求后端数据，request还做了code非200的统一处理，自己只需要关心调用成功后的处理逻辑；

## ListComponent

* 路径：src/javascript/component/NEKListComponent.js

## BaseModal



