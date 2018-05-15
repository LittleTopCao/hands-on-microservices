# 实战微服务的自动发现与负载均衡 

采用微服务架构后，巨无霸服务被拆分为若干逻辑独立的微服务，导致服务数量逐渐上升。此外，为了保证系统的高可用和高性能，每一个微服务都会运行若干副本，这更进一步地导致微服务运行实例数量的攀升。

面对数量逐渐攀升的微服务实例，我们不可能将服务的IP和端口都写在配置文件中，这种方案会使得系统无法维护。因此，采用微服务架构后，微服务服务（及实例）的自动发现是首先要解决的问题。

前面已经提到，出于高可用和高性能考量，微服务往往同时部署多个副本。如何实现自动负载均衡呢？这是本章要讨论的第二个重点。

本章将从容器技术谈起，介绍Docker和Kubernetes的优势。随后，我们会通过几个小例子，让大家快速上手Kubernetes。最后，我们结合一个微服务的实例，探讨如何利用Kubernetes的Service实现服务的自动发现与负载均衡。