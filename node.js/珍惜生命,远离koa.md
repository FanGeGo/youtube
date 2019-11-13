---
marp: true
style: |
  h1 {
    color: #0bb8e8;
  }
---

<style scoped>
h1,h2 {
	color: #0bb8e8;
	text-align: center
}
h2 {
	text-align: right
}

h3 {
  text-align:right;
  font-size:24px;
  margin-right:50px;
  color:#ccc
}

</style>

![h:48](./logo.png)
# 珍惜生命 远离koa
## :star:  田一块 

### 讨论普及社会常识（主要是政治，历史，科技）欢迎订阅

---
# 先看源码

## koa的中间件源码

```
const Koa = require('koa');
const app = new Koa();
app.use((ctx, next) => {
  next();
  ctx.body = "middleware 1\n";
});
app.use((ctx, next) => {
  next();
  ctx.body = "middleware 2\n";
});
app.use((ctx, next) => {
  ctx.body = "middleware 3\n";
});
app.listen(3000);
```

---
# 先看源码

## express的中间件源码

```
const express = require('express')
const app = express()
app.use((req, res, next) => {
  next();
  res.send("middleware 1\n");
});
app.use((req, res, next) => {
  next();
  res.send("middleware 2\n");
});
app.use((req, res, next) => {
  res.send("middleware 3\n");
});
app.listen(3000);
```

---

# 结果

## koa   :x:
```
middleware 1 
```
## express :heavy_check_mark:
```
middleware 3
```

## 你之的预期是什么?

---
# 原因有两点

## koa的中间件错误
## 过渡封装

---

# 中间件设计错误

## 使用promise的目标是消除回调,而koa却保留了回调函数
## 不理解promise本身就是线性的中间件

对于koa来讲, next函数是多余与错误的.

正确的koa中间件应该是这样的:
```
app.use((ctx) => {
  ctx.body = "middleware 2\n";
});
```

> 具体如何实现基于promise的中间件,可以参考vig的实现

---

# 错误与过度的封装

在ctx里面封装了body, req, res等所有HTTP请求的核心组件.
导致了第一个中间件可以对这些内容为所欲为.
同时更致命的是body的处理是在最外圈处理的.
也就是说ctx.body的最终处理,其实不是在核心处理,相反,他们最外面处理的.
所以koa最后一个中间件才是koa执行的核心.

---


# HTTP执行

正常的中间件下的HTTP请求

```
Request -> M1 -> M2 -> M3 -> ... -> Mn -> Response(content)
```

所以对于一个HTTP请求,在koa里是这样的.
```
Requst -> Koa -> M1 -> M2 -> M3 -> ... -> Mn -> (Content Generator) -> M'n(content) ... -> M'3(content) -> M'2(content) -> M'1(content) -> Koa(content) -> Response(content)
```

---
# HTTP请求与中间件的关系

## 正常中间件
> 不能对最终输出进行修改

## Koa的中间件
> 可以修改最终输出

---

# 安全风险

> 由于任何一个中间件都可以获得并修改输出结果,任何koa的中间件都是极度危险的中间件.

koa中间件的可实施黑客行为:

1. 获得用户最终输出内容,并发送到自己的服务器
2. 修改用户的输出结果,植入各种攻击代码.




