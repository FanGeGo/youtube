<span style="color:#3A9">Web全栈与前后端统一语言开发</span><p style="text-align:right;font-size:28px;margin-right:50px;color:#333388;">:star: 李白，字一日</p><p style="text-align:right;font-size:24px;margin-right:50px;color:#ccc">讨论普及社会常识（主要是政治，历史，科技）欢迎订阅</p>
===

---

什么是Web全栈？
==
全栈的概念最近非常火，主要是因为Facebook的工程师声称他们都是招全栈工程师的。
但是全栈工程师是什么呢？
全栈工程师其实是针对解决问题的能力来讲的，就是要求一个工程师能在多个方面发挥他的技能。
对于Web全栈工程师来讲，就是至少要懂前端与后端。当然如果你懂专业的图形，数据库，运维技术等技术当然是最好的。
但是前后端的基本技术是比较核心的。

---

前后端统一语言
==

随着Web技术的不断发展，前端技术越来越成为Web技术中的重要部分。
同时越来越多的开发集中到了前端。
而前端后端通用的逻辑就会越来越多。
这个时候共享前后端代码，减少冗余开发的要求就提上了议事日程。
而当Node.js出现后，第一次解决了前后端统一语言的问题。
让Javascript一个语言来处理整个网站成了可能。

---
Javascript的问题
==
但是Javascript仍有不少问题。最大的问题是Javascript的性能不行。
性能不行导致了Web技术无法实现大型的在线3D游戏或者计算密集型的应用。
同时其它的后端语言怎么办呢？
于时Web Assembly出现了。

---
Web Assembly前的努力
==
最初提升Javascript性能的方案有:
asm.js vs emscripten
asm.js是将js精简成一个子集，从而提高js的性能
emscripten是将C/C++的代码直接转化成javascript的代码

这两个性能方面的努力并不引人注意。

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
其它语言操作DOM（包括BOM)的问题，有了Web Assembly任何语言都可以编写操作HTML/CSS的代码。
这样前后端统一语言就成为了可能。

目前支持Web Assembly的语言已经有很多了。
常规的语言大部分都可以很好的支持。
