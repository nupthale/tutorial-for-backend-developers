# 快速起步

> 示例：[http://regularjs.github.io/guide/zh/intro/hello-regularjs.html](http://regularjs.github.io/guide/zh/intro/hello-regularjs.html)

[Demo](http://fiddle.jshell.net/leeluolee/C2Gh9/1/)

1. 通过script引入Regularjs；引入后，就可以直接通过Regular变量访问到Regular对象了；
2. 工程所有的组件都是Regular.extend出来的，为了提取一些通用的东西，我们又封装了BaseComponent， BaseComponent继承于Regular，工程中所有组件都从BaseComponent进行扩展；

   ```
    ![](/assets/popo_2017-06-23  13-47-22.jpg)
   ```

3. 几个关键属性和方法

```
template: 组件的模板
data: component组件的初始化状态；
$inject方法：会将组件插入到目标节点的位置
```



