<span style="color:#3A9">各种端与App什么关系？</span><p style="text-align:right;font-size:28px;margin-right:50px;color:#333388;">:star: 李白，字一日</p><p style="text-align:right;font-size:24px;margin-right:50px;color:#ccc">讨论普及社会常识（主要是政治，历史，科技）欢迎订阅</p>
===
---

经常讨论的端
===
1. 前端、后端
2. 客户端、服务器端
3. 桌面端

---
基于C/S模式的端分类
===

#### 图解

$$ Ends \left \{
\begin{aligned}
Client \left \{
\begin{aligned}
Generic \ Clients \left \{
\begin{aligned}
Desktop\\
Mobile \ \   
\end{aligned}
\right.\\
Browsers \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ 
\end{aligned}
\right. \\
\\
Server \left \{
\begin{aligned}
Raw \ TCP/UDP \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \\
HTTP/WebSocket\ \ \ \ \ \ \ \ \ \ \ \ \ 
\end{aligned}
\right.
\end{aligned}
\right.
$$

---
基于C/S模式的端分类
===

#### ==*客户端*==
1. 常规客户端（移动/桌面）
2. 浏览器端（移动/桌面）
#### ==*服务器端*== 
1. 常规TCP/UDP服务器
2. Web服务器

---
客户端与服务器端的差别
===
1. 通常一个**客户端**只能服务于一个**用户**
2. 通常一个**服务器端**能服务于多个**客户端**

---
基于B/S模式的端分类
===
$$ Ends \left \{
\begin{aligned}
Frontend(Browser) \left \{
\begin{aligned}
HTML \ \ \ \ \ \ \ \ \ \ \ \ \ \ \\
CSS \ \ \ \  \ \ \ \ \ \ \ \ \ \ \ \ \ \  \\
Javascript \ \ \ \ \ \ \ \ 
\end{aligned}
\right. \\
\\
Backend(Server) \left \{
\begin{aligned}
Web \ Server \ \ \ \ \ \ \ \ \ \ \ \ \\
Database  \ Server \ \ \ \ \\
Cache \ Server \ \ \ \ \ \ \ \ \ \\
etc. \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \ \ \ \ 
\end{aligned}
\right.
\end{aligned}
\right.
$$

---
基于B/S模式的端分类
===
通常我们基于B/S将我们的应用环境分成前后端。

1. 前端是HTML+CSS+JS组成的浏览器环境
2. 后端是提供服务的各种服务器

所以我们可以看到：
> 前后端主要是针对B/S架构来说的。

---

B/S与C/S有什么区别？
===
1. 固定的协议
B/S有、C/S没有
2. 通用的解析器
B/S有、C/S没有
3. 开放性
B/S好，C/S差
4. 成熟度
B/S好，C/S差。

趋势： C/S =》 B/S

---

什么是Web技术？
===

Web技术是对基于HTTP技术的一系列技术的统称。
Web技术基本上与B/S技术是一致的。

通常:

B端 => 前端
S端 => 后端

---

前端
===
即浏览器端。

主要是指基于浏览器的技术。

以HTML+CSS+JS为基础的技术。

---

后端
===
即服务器端。

通常由：
1. HTTP服务器
2. 服务器动态脚本（Java, PHP, Python, Ruby, Node.js)
3. 数据库服务器
4. 缓存服务器
5. 其它各种服务器组合
等组成。

---

我在那个端开发App？
===
1. 客户端应用
浏览器，Android/iOS Mobile App, WIN32/Mac OS/Linux Desktop
2. 服务器端
Nginx/Apache, WIN32 Web Server, Mac OS Web Server, Linux Web Server

> 我们可以发现，属于那个端，有时候非常清楚，有时候并没有那么明确的。只有当具体的应用场景出现时，我们才能完全分清楚。


---
App各种端是什么关系？
===
App是一种面向最终用户的说法。以功能为目的进行分割的。比如微信。
端是一种面向技术的说法。以硬件或者软件环境为分割的。比如手机端。

所以说App与各种端是互不隶属的关系。
但是App可能存在于任何一个端中。

---
实际的端案例
===

1. 浏览器通常无法创建HTTP服务器，所以通常只能是客户端。
2. Apache/Nginx通常不会运行在浏览器，所以是服务器端，也是后端。
3. 但是当我们在Android手机上开发了FTP功能时，实际上在Android上建立了FTP服务器，所以虽然Android通常是开发客户端，但是也可以是服务器。
4. ionic目前只能做客户端，又因为它主要采用的是Web技术，所以也可以看成是Web前端。
---









