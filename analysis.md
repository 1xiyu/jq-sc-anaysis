v2.0.3
###  立即执行
(function( window, undefined ) {})(window)？

1 解决命名空间和变量污染
2 减少查找经过的scope，window在闭包内当做局部使用
3 undefined ?  debug ie8  undefined 可定义

### 无new构建

 return new jQuery.fn.init( selector, context, rootjQuery );

 分割作用域的原理：每次构建新的init

 jQuery.fn.init.prototype = jQuery.fn;

 jQuery的原型覆盖jQuery原型的init上的原型。

### 链式调用

 return this  

 简单工厂模式，同一个dom指定同一个实例

### 插件接口

jQuery.extend = jQuery.fn.extend = function() {}

不会破坏 jQuery.prototype  

借助this实现不同的功能 调用jQuery.extend this指向jQuery 调用jQuery.fn.extend this指向jQuery.fn 