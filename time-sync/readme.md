### time-sync 为什么开发一个时间同步服务
开发某次找我说我们本地kubernetes集群内的pod时间和阿里云标准时间差值大于5秒了，导致阿里接口校验失败，我发现的确本地集群node时间会跑偏，于是开发了时间同步服务，用于阿里云集群节点时间自动校准,采用DaemonSets部署方式，每个节点长驻一个时间同步服务
### 提供版本
- windows x86_64
- linux x86_64
- Kubernetes x86_64
  - Dockerfile
  - DaemonSets yaml
### 如有疑问请联系作者
- E-Mail/QQ: 46603415@qq.com
