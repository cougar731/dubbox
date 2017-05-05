Dubbo: 分布式通讯框架
======================================
Dubbo是一个高性能的分布式RPC框架，主要包括一下部分:

* Remoting(远程通信): a network communication framework provides sync-over-async and request-response messaging.
* Clustering(集群): a remote procedure call abstraction with load-balancing/failover/clustering capabilities.
* Registry(注册中心): a service directory framework for service registration and service event publish/subscription


### 和Dubbo 2.x的区别

* Java 8 only, hessian序列化支持Java 8 Optional
* 序列化调整到hessian2协议上
* zookeeper有zkClient调整到curator
* Spring Boot兼容
* 注册中心: 删除simple registry
* 通讯协议: 默认Netty4， 删除thrift，http，Grizzly，rmi等协议支持
* 容器: 取消Jetty支持，使用Spring Boot替换
* Docker: 在 Protocol 配置中增加了 exportHost 和 exportPort 参数, 区分容器内绑定的真实地址和注册到注册中心的宿主机地址

