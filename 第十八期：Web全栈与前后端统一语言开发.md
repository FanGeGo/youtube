<span style="color:#3A9">Web全栈与前后端统一语言开发</span><p style="text-align:right;font-size:28px;margin-right:50px;color:#333388;">:star: 李白，字一日</p><p style="text-align:right;font-size:24px;margin-right:50px;color:#ccc">讨论普及社会常识（主要是政治，历史，科技）欢迎订阅</p>
===

---

什么是Web全栈？
==
全栈的概念已经提出来很多年了，但是最近似乎仍非常 火

主要是因为这是Facebook的工程师提出来的

声称他们都是招全栈工程师的

全栈工程师主要是指一个工程师能解决多种问题

对于Web全栈工程师来讲，就是至少要能解决前端与后端的问题

所以要成为Web全栈工程师，优先要掌握前后端的基本技术

---

前后端统一语言
==

由于在Web开发过程中，前后端的很多逻辑可能是一样的

如果能够共享前后端代码，减少冗余开发就最好了

这个时候Node.js横穿出世，完美解决了这一问题

让一种语言来处理整个网站开发成了可能。

---
Javascript的问题
==
但是Javascript有一个致命的问题：

性能问题，导致实现

1. 实现大型的在线3D游戏
2. 计算密集型的应用

的功能困难

那么有没有解决办法？

---
Javascript性能提升问题的解决方案
==
最初提升Javascript性能的方案有:
asm.js vs emscripten
asm.js是将js精简成一个子集，从而提高js的性能
emscripten是将C/C++的代码直接转化成javascript的代码

但是这两个性能方面的努力并不引人注意。

---
Web Assembly的出现
==

直到ES6+的出现。ES6+新增强的很多JS特性是非常破坏性的。比如generator，直接破坏了JS的语法的美感。
（后来async/await关键字的引入解决了这个问题）
因为\*号在JS里是运算符号，而却被当成是语法了。

后来国内一开发者发表了对ES6+语法过渡被多种语言背景的人撕裂的看法，同时提出了解决方案：即一个语言中立的抽象层，直接操作DOM/BOM的构想。

3个月后，W3C成立了Web Assembly工作组。

---
Web Assembly的进展
==

Web Assembly解决了:

1. 语言中立的问题，
2. 性能问题
3. DOM操作问题(仍在开发中)

这样未来前后端统一语言就成为了一种潮流

目前支持Web Assembly的语言已经有很多了。
常规的语言大部分都可以很好的支持。
