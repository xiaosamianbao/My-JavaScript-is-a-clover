#我的JavaScript是一朵三叶草
----
JavaScript由ECMAScript、DOM（Document Object Model）、BOM（Browser Object Model）三部分组成；其中ECMAScript定义了JS的书写规范和语法；BOM可以操作与浏览器的交互；DOM可以让我们操作网页的内容；根据宿主（浏览器）的不同，具体的表现形式也不尽相同，ie和其他的浏览器风格不同。

javacsript是通过访问BOM对象来访问、控制、修改客户端(浏览器);window对象的属性和方法是直接可以使用而且被感知的;由于BOM的window包含了document，因此可以直接使用window对象的document属性；通过document属性就可以访问、检索、修改XHTML文档内容与结构。因为document对象又是DOM模型的根节点。

可以说，BOM包含了DOM(对象)，浏览器提供出来给予访问的是BOM对象，从BOM对象再访问到DOM对象，从而JavaScript可以操作浏览器以及浏览器读取到的文档。
<a name="table-of-content"></a>

JavaScript中我们学的所有的知识点其实都是基于浏览器内置类实现的，这也说明了js是由一个个类组成的，而我们要学习的就是类、实例的关系和类上面的私有或者公有的属性或者方法---这就是我们经常听到的面向对象编程
##目录
# 1、ECMAScript #
由ECMA-262定义，提供核心语言功能。

1. [基本概念](#test)
    + 语法规范
    + 关键字和保留字
    + 变量命名、声明、变量类型、作用域、闭包、垃圾回收机制
    + 数据类型（基本数据类型和引用数据类型）
    + 运算符/操作符
    + 流程语句（循环、跳转、判断/选择、异常处理）
    + 函数的参数理解
    + 定时器
1. [预解释](#test)
    + 语法规范
    + 关键字和保留字
    + 变量
    + 数据类型
1. [this关键字和函数表达式](#test)
    + 定义
    + 调用
    + 方法call和apply
    + arguments
    + 函数参数指针标识
1. [深入解读具体的引用数据类型以及它们的方法](#test)
    + Object类型
    + Array类型
    + Date类型以及日历控件
    + RegExp
    + Function类型
    + 基本包装类型（Boolean/Number/String）
    + 单体内置对象（Global对象/Math对象）
1. [面向对象的程序设计](#test)
    + 面向对象
    + 创建对象
    + 继承
    + 使用面向对象的思想扩展数组类
1. [JSON数据高20](#test)
    + 模块化开发
    + 模块化开发
1. [兼容性处理、错误处理与调试高17章](#test)
    + 模块化开发
    + 模块化开发


# 2、DOM #
文档对象模型，提供访问和操作网页内容的方法和接口，DOM 是W3C的标准；所有浏览器公共遵守的标准。

1. [节点获取](#test)
    + 通过上下文获取节点
    + 通过节点指针获取节点
1. [节点操作](#test)
    + 增删改查
1. [属性操作](#test)
    + 获取属性
    + 设置属性
    + 判断属性
1. [文本操作](#test)
    + 获取属性
    + 设置属性
    + 判断属性
1. [JS中的盒子模型](#test)
    + 盒子模型
    + 图片加载机制
    + 图片延迟加载实例
1. [自己动手封装DOM库](#test)
    + 单例子模式
    + 构造函数模式
    + 构造函数模式2
1. [案例练习](#test)
    + 模块化开发之日历控件开发
    + 模块化开发之选项卡组件
1. [事件](#test)
    + 事件的实现（事件的绑定）
    + DOM元素的默认行为
    + 事件传播和阻止事件传播
    + 事件委托
1. [DOM二级事件](#test)
    + DOM2和DOM3
    + 事件的常见兼容性问题总结
    + DOM二级时间兼容性问题解决质疑：this关键字；
    + DOM二级时间兼容性问题解决质疑：执行顺序问题；
1. [拖拽效果](#test)
    + 拖拽效果的编写和优化
    + 写在HTML标签里的事件是 如何被浏览器解析并执行的
    + 给拖拽加效果并且发现代码在设计思想上的问题；
    + 优化上一章讲的事件库；
    + 给拖拽加更多动画效果；
1. [照片墙示例](#test)
    + 基于模块化开发
    + 观察者模式
    + 面向对象及原型的继承；
    + 事件原理；
    + 事件库；

# 3、BOM #

提供与浏览器交互的方法和接口，BOM 是 各个浏览器厂商根据 DOM在各自浏览器上的实现;[表现为不同浏览器定义有差别,实现方式不同]。

BOM的核心是window，而window对象又具有双重角色，它既是通过js访问浏览器窗口的一个接口，又是一个Global（全局）对象。这意味着在网页中定义的任何对象，变量和函数，都以window作为其global对象。

BOM主要是学window对象；window包括以下

1. [对话框](#test)
    + 模块化开发
    + 模块化开发
1. [定时器](#test)
    + 模块化开发
    + 模块化开发
1. [焦点控制](#test)
    + 模块化开发
    + 模块化开发
1. [窗口控制](#test)
    + 模块化开发
    + 模块化开发
1. [打开关闭窗口](#test)
    + 模块化开发
    + 模块化开发
1. [属性](#test)
    + 模块化开发
    + 模块化开发
1. [navigation 导航器对象](#test)
    + 模块化开发
    + 模块化开发
1. [screen 显示器对象](#test)
    + 模块化开发
    + 模块化开发
1. [history 历史对象](#test)
    + 模块化开发
    + 模块化开发
1. [location 位置对象](#test)
    + 模块化开发
    + 模块化开发
1. [document 文档对象](#test)
    + 模块化开发
    + 模块化开发
1. [客户端检测高9章](#test)
    + 模块化开发
    + 模块化开发

1. [HTTP](#test)
    + WEB客户端和服务器
    + HTTP事务
    + HTTP报文
    + HTTP方法
    + GET和POST的区别
    + HTTP状态码
    + MIME Type
    + URI、URL、URN
1. [AJAX与Comet](#test)
    + 什么是AJAX
    + 网页渲染的同步和异步区别
    + 浏览器兼容性
    + 如何发起AJAX
    + 使用XMLHttpRequest
    + 在低版本IE浏览器中使用ActiveXObject时需要注意的地方
    + 模仿jQuery封装AJAX库
    + 表单操作/表单脚本高三14章
    + 利用AJAX模拟表单提交
    + 跨域请求操作
    + W3C规定的跨域资源共享中服务器可以返回的头信息
1. [离线应用与客户端存储高23章](#test)
    + 离线监测
    + 应用缓存
    + 数据存储
1. [高级技巧高22章](#test)
    + 高级函数
    + 防篡改对象
    + 高级定时器
    + 自定义事件
    + 拖放
1. [最佳实践高24章](#test)
    + 可维护性
    + 性能
    + 部署

**[↑ 返回目录](#table-of-content)**

如果把JavaScript看成三叶草的话，那么jQuery就是三叶草的第四片叶子

jQuery is fourth leaves of JavaScript