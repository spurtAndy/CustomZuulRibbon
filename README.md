# CustomZuulRibbon
自定义Zuul的路由规则，自定义listOfServer来源，自定义ribbon的IRule、IPing、ServerList等。
## 前言
脱离Eureka等服务注册与发现组件，使用Zuul和Ribbon来做网关负载均衡，可以在application.properties中配置listOfServer指定后台主机地址。
然而这种方式强依赖配置文件，无法做到实时变更和维护。通过构建自定义的路由加载、service-id的一些配置来实现从数据库加载路有规则，
同时可以配置自定义的ServerList、IRule、IPing等类来维护网关的可扩展性。
