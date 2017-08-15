# SPDY协议

![HTTP-bottleneck](../assets/SPDY.png)

- 原理：在SSL层上增加一个SPDY会话层，以在一个TCP连接中实现并发流。SSL层上增加SPDY会话层通常的HTTP GET和POST格式仍然是一样的；然而SPDY为编码和传输数据设计了一个新的帧格式。流是双向的，可以在客户端和服务器端启动。SPDY旨在通过基本（始终启用）和高级（可选启用）功能实现更低的延迟。
- 功能：
  1. 多路复用：在一条TCP连接中并发多个请求，防止请求的阻塞
  2. 赋予请求优先级
  3. 压缩HTTP首部
  4. 服务器推送功能：赋予服务器主动向客户端推送数据的功能
  5. 服务器提示功能：服务器可以主动提示客户端需要请求的资源
- 现状：已被 HTTP/2 取代