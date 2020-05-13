---
title: 微服务实践
layout: post
---

# 背景
## Nginx负载均衡集群服务
分散成了N个服务，每个服务又是一个集群，对于一个大项目来说，维护这些配置是非常头疼的。笔者曾经在某知名互联网公司工作过，公司最累最背锅的就是运维团队，基本24小时都在应付各个团队的部署上线工作以及各种配置的维护，而且还经常出错挨骂。那么服务治理就出现在这种应用场景之中，运维工程师不用再维护各个负载均衡节点，由服务中心去统一处理。

# 实现方式
### .NetCore

1.SpringCloud+.NetCore
(Spring Eureka+SteeltoeOSS)
http://www.csharpkit.com/2017-09-24_52002.html
http://www.csharpkit.com/2017-09-24_99589.html

2.Ocelot(网关、限流、熔断、熔错告警、限流)+Consul(发现和注册、熔断、负载均衡)