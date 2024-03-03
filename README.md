# 基于 gRPC 的远程方法调用。

通过 protocol buffer 的语法定义通信数据的格式，比如 package、service 等。

然后 server 端实现 service 对应的方法，client 端远程调用这个 service。

比如在 java 的 spring 里，需要安装这两个依赖：

![https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/95ac4d74e3984ac7bce3ed1e5bdfe21b~tplv-k3u1fbpfcp-jj-mark:2722:0:0:0:q75.awebp#?w=1256&h=252&s=60129&e=png&b=f4f6fa](image.png)

然后也是定义这样的 proto 文件：

![https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f27f966938ae4fb798eef7b9a54acc60~tplv-k3u1fbpfcp-jj-mark:2722:0:0:0:q75.awebp#?w=1168&h=1030&s=172873&e=png&b=f4f6fa](image.png)

之后定义对应的 service：

![https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f34e2518db424f65af445e2dfda82e32~tplv-k3u1fbpfcp-jj-mark:2722:0:0:0:q75.awebp#?w=1596&h=942&s=190072&e=png&b=f3f5f9](image.png)

和 node 里差不多。

这样就可以实现在 java、node、go、python 等多种语言之间实现微服务的远程方法调用。