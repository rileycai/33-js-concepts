<h1 align="center">
<br>
  <a href="https://github.com/stephentian/33-js-concepts"><img src="33_js_concepts.jpg" alt="每位 JS 开发应该懂的 33 个概念" width=200"></a>
  <br>
    <br>
  JavaScript开发者应懂的33个概念
  <br>
</h1>

## 简介

这个项目是为了帮助开发者掌握 JavaScript 概念而创立的。它不是必备，但在未来学习（JavaScript）中，可以作为一篇指南。

> 本篇文章是参照 @leonardomso 创立，英文版项目地址在[这里](https://github.com/leonardomso/33-js-concepts)。

> 由于原版资源都要翻墙，所以本人创立一个中文版，附上关于这些概念在国内的一些文章和视频。

> 文章的排序我也优化了一下，前面的文章是介绍概念，后面的文章是深入解读。

> 若有觉得更好的文章或者视频，可以贡献出来，觉得有误的，请联系我删除。

---

## 目录

- **[调用堆栈](#调用堆栈)**
- **[原始类型](#原始类型)**
- **[值类型和引用类型](#值类型和引用类型)**
- **[隐式, 显式, 名义和鸭子类型](#隐式-显式-名义和鸭子类型)**
- **[==, ===, typeof 的比较](#vs-vs-typeof)**
- **[this, call, apply 和 bind](this-call-apply-和-bind)**
- **[函数作用域, 块级作用域和词法作用域](#函数作用域-块级作用域和词法作用域)**
- **[闭包](#闭包)**
- **[递归](#递归)**
- **[算法](#算法)**
- **[map, reduce, filter](#map-reduce-filter)**
- **[表达式和语句](#表达式和语句)**
- **[变量提升](#变量提升)**
- **[高阶函数](#高阶函数)**
- **[立即执行函数, 模块化, 命名空间](#立即执行函数-模块化-命名空间)**
- **[数据结构](#数据结构)**
- **[消息队列和事件循环](#消息队列和事件循环)**
- **[setTimeout, setInterval 和 requestAnimationFrame](#settimeout-setinterval-和-requestanimationframe)**
- **[继承, 多态和代码复用](#继承-多态和代码复用)**
- **[按位操作符, 类数组对象和类型化数组](#按位操作符-类数组对象和类型化数组)**
- **[DOM 树和渲染过程](#DOM-树和渲染过程)**
- **[new 与构造函数, instanceof 与实例](#new-与构造函数-instanceof-与实例)**
- **[原型继承与原型链](#原型继承与原型链)**
- **[Object.create 和 Object.assign](#objectcreate-和-objectassign)**
- **[工厂函数和类](#工厂函数和类)**
- **[设计模式](#设计模式)**
- **[Memoization](#memoization)**
- **[纯函数, 函数副作用和状态变化](#纯函数-函数副作用和状态变化)**
- **[耗性能操作和时间复杂度](#耗性能操作和时间复杂度)**
- **[JavaScript 引擎](#javascript引擎)**
- **[二进制, 十进制, 十六进制, 科学记数法](#二进制-十六进制-十进制-科学记数法)**
- **[偏函数, 柯里化, Compose 和 Pipe](#偏函数-柯里化-compose-和-pipe)**
- **[代码整洁之道](#代码整洁之道)**

---

## 调用堆栈

### 文章

- :book: [Call Stack — MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
- :book: [并发模型与事件循环 —— MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/EventLoop)
- :book: [JavaScript 运行机制详解：再谈 Event Loop —— 阮一峰](http://www.ruanyifeng.com/blog/2014/10/event-loop.html)
- :book: [深入理解 JavaScript 事件循环 —— 博客园](https://www.cnblogs.com/dong-xu/p/7000163.html)
- :book: [深入浅出 Javascript 事件循环机制 —— 知乎](https://zhuanlan.zhihu.com/p/26229293)
- :book: [JS 事件循环机制（event loop）之宏任务、微任务 —— SegmentFault](https://segmentfault.com/a/1190000014940904#articleHeader7)
- :book: [JavaScript：彻底理解同步、异步和事件循环 —— SegmentFault](https://segmentfault.com/a/1190000004322358)
- :book: [[译] JavaScript 如何工作：对引擎、运行时、调用堆栈的概述 —— 掘金](https://juejin.im/post/5a05b4576fb9a04519690d42#comment)
- :book: [[译] 理解 JavaScript 中的执行上下文和执行栈 —— 掘金](https://juejin.im/post/5ba32171f265da0ab719a6d7)
- :book: [这一次，彻底弄懂 JavaScript 执行机制 —— 掘金](https://juejin.im/post/59e85eebf265da430d571f89)
- :book: [解读 JavaScript 之引擎、运行时和堆栈调用 —— 开源中国](https://www.oschina.net/translate/how-does-javascript-actually-work-part-1)
- :book: [Tasks, microtasks, queues and schedules —— Jake Archibald](https://jakearchibald.com/2015/tasks-microtasks-queues-and-schedules/)

### 视频

- :tv: [What is the event loop anyway? —— 腾讯视频(英文字幕)](https://v.qq.com/x/page/h0372bld8re.html?ptag=qqbrowser)
- :tv: [Understanding The JavaScript Call Stack, Event Queue, Event Table, & Event Loop —— Bilibili](https://www.bilibili.com/video/av33824933/)
- :tv: [JS 中的变量提升、堆栈内存及闭包详解 —— Acfun](http://www.acfun.cn/v/ac4495641)
- :tv: [事件循环模型 —— PHP 中文网](http://www.php.cn/code/21194.html)

**[:arrow_up: back_to_up](#目录)**

---

## 原始类型

### 文章

- [原始数据 —— MDN](https://developer.mozilla.org/zh-CN/docs/Glossary/Primitive)
- [ECMAScript 原始类型 —— W3school](http://www.w3school.com.cn/js/pro_js_primitivetypes.asp)
- [How numbers are encoded in JavaScript —— Dr. Axe](http://2ality.com/2012/04/number-encoding.html)
- [每一个 JavaScript 开发者应该了解的浮点知识 —— 颜海镜](https://yanhaijing.com/javascript/2014/03/14/what-every-javascript-developer-should-know-about-floating-points/)
- [JavaScript 标准参考教程(基本语法之数值) —— 阮一峰](https://wangdoc.com/javascript/types/number.html)
- [The Secret Life of JavaScript Primitives —— Angus Croll](https://javascriptweblog.wordpress.com/2010/09/27/the-secret-life-of-javascript-primitives/)

### 视频

- [javascript 六种数据类型 —— 慕课网](https://www.imooc.com/video/5674)
- [javascript 视频教程(数据类型) —— PHP 中文网](http://www.php.cn/code/5808.html)

**[:arrow_up: back_to_up](#目录)**

---

## 值类型和引用类型

### 文章

- :book: [ECMAScript 引用类型 —— W3school](http://www.w3school.com.cn/js/pro_js_referencetypes.asp)
- :book: [js 中的值类型和引用类型的区别 —— 博客园](https://www.cnblogs.com/leiting/p/8081413.html)
- :book: [JavaScript 的值传递和引用传递 —— FunDebug](https://blog.fundebug.com/2017/08/09/explain_value_reference_in_js/)
- :book: [Primitive Types & Reference Types in JavaScript —— Bran van der Meer](https://docstore.mik.ua/orelly/webprog/jscript/ch04_04.htm)
- :book: [JavaScript: Passing by Value or by Reference —— CSDN](https://blog.csdn.net/xiaojia_boke/article/details/54906509)
- :book: [js 值引用和值复制 —— SegmentFault](https://segmentfault.com/a/1190000015411195)
- :book: [js- 引用和复制(传值和传址) —— CSDN](https://blog.csdn.net/zzzaquarius/article/details/4902235)

**[:arrow_up: back_to_up](#目录)**

---

## 隐式, 显式, 名义和鸭子类型

### 文章

- [ECMAScript 类型转换 —— W3school](http://www.w3school.com.cn/js/pro_js_typeconversion.asp)
- [JavaScript 的怪癖 1：隐式类型转换 —— justjavac](http://justjavac.com/javascript/2013/04/08/javascript-quirk-1-implicit-conversion-of-values.html)
- [JavaScript 运算符规则与隐式类型转换详解 —— 掘金](https://juejin.im/post/59ad2585f265da246a20e026)
- [聊一聊 JS 中的隐式类型转换 —— SegmentFault](https://segmentfault.com/a/1190000004482388)
- [有趣的 JavaScript 隐式类型转换 —— 博客园](https://www.cnblogs.com/yugege/p/5277883.html)
- [JavaScript 显式类型转换与隐式类型转换 —— CSDN](https://blog.csdn.net/yangjvn/article/details/48284163)
- [你不知道的 JavaScript（中卷）强制类型转换 —— 简书](https://www.jianshu.com/p/777a89b4ed9a)
- [你懂 JavaScript 嗎？#8 強制轉型 —— cythilya](https://ithelp.ithome.com.tw/articles/10201512)
- [动态类型语言和鸭子类型 —— 曾探](http://book.51cto.com/art/201505/475153.htm)
- [Nominal & Structural Typing —— flow](https://flow.org/en/docs/lang/nominal-structural/)
- [What exactly is Type Coercion in Javascript? —— stackoverflow](https://stackoverflow.com/questions/19915688/what-exactly-is-type-coercion-in-javascript)
- [You Don't Know JS: Types & Grammar —— github](https://github.com/getify/You-Dont-Know-JS/blob/master/types%20&%20grammar/ch4.md)

### 视频

- [javascript 隐式转换 —— 慕课网](https://www.imooc.com/video/5675)
- [Javascript 基础加强-类型转换 —— 黑马程序员](http://www.le.com/ptv/vplay/27767009.html?ch=baidu_s)

**[:arrow_up: back_to_up](#目录)**

---

## == vs === vs typeof

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## this, call, apply 和 bind

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 函数作用域, 块级作用域和词法作用域

### 文章

- [变量作用域与解构赋值 —— 廖雪峰](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/0014344993159773a464f34e1724700a6d5dd9e235ceb7c000)
- [学习 Javascript 闭包（Closure） —— 阮一峰](http://www.ruanyifeng.com/blog/2009/08/learning_javascript_closures.html)
- [JavaScript 中词法作用域、闭包与跳出闭包 —— SegmentFault](https://segmentfault.com/a/1190000006671020)
- [JavaScript 深入之词法作用域和动态作用域 —— 掘金](https://juejin.im/entry/58e70077b123db15eb88dc7e)
- [深入理解闭包之前置知识 → 作用域与词法作用域 —— 掘金](https://juejin.im/post/5afb0ae56fb9a07aa2138425)
- [What is lexical scope? —— stackoverflow](https://stackoverflow.com/questions/1047454/what-is-lexical-scope)
- [You Don't Know JS: Scope & Closures —— Kyle Simpson](https://github.com/fishenal/You-Dont-Know-JS/blob/master/scope%20&%20closures/ch2.md)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 闭包

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## map, reduce, filter

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 表达式和语句

### 文章

- [js 表达式与语句 —— 博客园](https://www.cnblogs.com/xianshenglu/p/8386918.html)
- [JS 表达式和语句的区别 —— SegmentFault](https://segmentfault.com/q/1010000004102804)
- [JavaScript 中的表达式（expression）和语句/声明（statement） —— CSDN](https://blog.csdn.net/mett_smith/article/details/78761247)
- [重讀 Axel 的 Javascript 中的 Expression vs Statement 一文 —— SegmentFault](https://segmentfault.com/a/1190000004565693)
- [Expressions versus statements in JavaScript —— Dr. Axel](http://2ality.com/2012/09/expressions-vs-statements.html)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 变量提升

### 文章

- [JavaScript 变量提升 —— 菜鸟教程](http://www.runoob.com/js/js-hoisting.html)
- [ES6 变量作用域与提升：变量的生命周期详解 —— 掘金](https://juejin.im/post/59905bea6fb9a03c34192c51)
- [[翻译] JavaScript Scoping and Hoisting —— SegmentFault](https://segmentfault.com/a/1190000004345355#articleHeader5)
- [JavaScript Scoping and Hoisting —— Ben Cherry](http://www.adequatelygood.com/JavaScript-Scoping-and-Hoisting.html)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 高阶函数

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 立即执行函数, 模块化, 命名空间

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 数据结构

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 消息队列和事件循环

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## setTimeout, setInterval 和 requestAnimationFrame

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 继承, 多态和代码复用

### 文章

- [代码复用模式 —— github](https://github.com/TooBug/javascript.patterns/blob/master/chapter6.markdown)
- [深入理解 JavaScript：代码复用模式(推荐篇) —— 汤姆大叔](http://www.cnblogs.com/TomXu/archive/2012/04/24/2438050.html)
- [深入理解 JavaScript：代码复用模式(避免篇) —— 汤姆大叔](https://www.cnblogs.com/TomXu/archive/2012/04/23/2438005.html)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 耗性能操作和时间复杂度

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## JavaScript 引擎

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 二进制, 十六进制, 十进制, 科学记数法

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 按位操作符, 类数组对象和类型化数组

### 文章

- [按位操作符 —— MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators)
- [类数组对象 —— MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Typed_arrays)
- [类型化数组 —— MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer)
- [JavaScript ArrayBuffer 浅析 —— 博客园](https://www.cnblogs.com/gradolabs/p/4762134.html)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## DOM 树和渲染过程

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## new, 构造函数, instanceof 和实例

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 原型继承与原型链

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## Object.create 和 Object.assign

### 文章

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 工厂函数和类

### 文章

- [类 —— MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Classes)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 设计模式

### 文章

- [JavaScript Patterns 中译本 —— github](https://github.com/lxj/javascript.patterns)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## Memoization

### 文章

- [JavaScript Memoization —— 司徒正美](https://www.cnblogs.com/rubylouvre/archive/2009/08/06/1540678.html)
- [memoization 提升递归效率 —— 博客园](https://www.cnblogs.com/yingshuizy/p/4517102.html)
- [如何提升 JavaScript 的递归效率 —— 51CTO](http://developer.51cto.com/art/201010/231513.htm)
- [JavaScript 高级技巧 Memoization —— SegmentFaut](https://segmentfault.com/a/1190000016703106)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 纯函数, 函数副作用和状态变化

### 文章

- [纯函数(Pure Function) —— React.js 小书](http://huziketang.mangojuice.top/books/react/lesson32)
- [JavaScript Functional Programming：纯函数 —— 宁皓网](https://ninghao.net/blog/4634)
- [js 函数的副作用分析 —— 脚本之家](https://www.jb51.net/article/28079.htm)
- [如何使用纯函数式 JavaScript 处理脏副作用 —— 掘金](https://juejin.im/post/5b82bdb351882542e241ed32?utm_medium=hao.caibaojian.com&utm_source=hao.caibaojian.com)
- [原生 JavaScript 实现 state 状态管理系统 —— 博客园](http://www.cnblogs.com/zhangycun/p/9403335.html)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 偏函数, 柯里化, Compose 和 Pipe

### 文章.

- [JavaScript 专题之偏函数 —— SegmentFault](https://segmentfault.com/a/1190000010686144)
- [柯里化和偏函数有什么区别？ —— SegmentFault](https://segmentfault.com/q/1010000008626058)
- [Javascript 偏函数与柯里化 —— CSDN](https://blog.csdn.net/neweastsun/article/details/75947785?utm_source=blogxgwz0)
- [JavaScript 函数式编程之函数组合函数 compose 和 pipe 的实现 —— SegmentFault](https://segmentfault.com/a/1190000015102804)

### 视频

**[:arrow_up: back_to_up](#目录)**

---

## 代码整洁之道

### 文章

- [[译] JavaScript 代码整洁之道 —— 边城](https://www.zcfy.cc/article/clean-code-javascript-readme-md-at-master-ryanmcdermott-clean-code-javascript-github-2273.html)
- [重构 - 代码整洁之道 —— 掘金](https://juejin.im/post/5a5b2a5c6fb9a01cbc6e59f9)
- [让你的代码更简短，更整洁，更易读的 ES6 小技巧 —— 掘金](https://juejin.im/post/5a7d71836fb9a063435ecf51)
- [Web 前端：11 个让你代码整洁的原则 —— 伯乐在线](#http://blog.jobbole.com/23617/)

**[:arrow_up: back_to_up](#目录)**

---