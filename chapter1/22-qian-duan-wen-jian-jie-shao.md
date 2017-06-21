# 前端文件介绍

![](/assets/popo_2017-06-21  19-28-33.jpg)

前端文件位于工程中的`src/main/webapp`目录下，主要包括：

* src目录：

  * src/javascript: 所有的js目录

    * 【不建议修改】javascript/base: 只有一个util文件，常用的util方法，如获取url中的param参数、合并merge两个对象等；不要在base下面增加新的文件；

    * 【不建议修改】javascript/component：全站通用组件，如类目选择组件、地址选择组件等放在component目录下；一般组件不要写在compenent目录下；放到各个页面中；

    * 【不建议修改】javascript/lib：依赖库目录，里面有regular、echarts、nek-ui、nej等；

    * 【不建议修改】javascript/widget：BaseComponent、全局filter、全局directive指令；所有js组件的基类都是这里的BaseComponnent；后面会详细介绍这些类；

    * **javascript/page**：页面的js文件；基本上一个页面的全部js逻辑都写在对应的目录下；在这里可以找到一个页面的完整的结构+样式+行为；

  * src/css: 工程基础样式目录, css目录下的page目录是老写法，新页面不要往里面加文件了；这里是全工程通用的样式文件，每个页面都会引入这些css，一般情况下不要修改css下的样式文件，除非确定是每个页面都要使用的样式；每个页面不同的样式文件会和页面的入口js放在一起；为什么这样做？是因为我们有NEKUI组件库，自己不太需要写样式，这样和js放在一起，找起来比较方便；

* WEB-INF/views目录：页面ftl目录

* 一些配置文件， 如.nekrc等；



