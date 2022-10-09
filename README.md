# devops

#### 介绍
运维工具集合,非开源,只提供二进制包

#### 目前提供的二进制包
##### time-sync 
- 为何开发
  - 开发某次找我说我们本地kubernetes集群内的pod时间和阿里云标准时间差值大于5秒了，导致阿里接口校验失败，我发现的确本地集群node时间会跑偏，于是开发了时间同步服务，用于阿里云集群节点时间自动校准,采用DaemonSets部署方式，每个节点长驻一个时间同步服务
- 提供版本
  - windows x86_64
    - 二进制文件
    - 默认配置文件
  - linux x86_64
    - 二进制文件
    - 默认配置文件
  - Kubernetes x86_64
    - Dockerfile
    - 二进制文件
    - 默认配置文件
    - DaemonSets yaml
##### rust-mysql-checker
- 为何开发
  - 开发某次给我说在k8s pod内连不上mysql,然后pod内又没有mysql客户端,也无法安装navicat类的可视化工具,所以运维需要快速判断mysql是否通畅(当然telnet也可以,但是不如这个工具直观),所以开发了此工具
- 提供版本
  - windows x86_64
    - 二进制文件
  - linux x86_64
    - 二进制文件
- 如何使用
  `./rust-mysql-checker 用户名 密码 host 端口 库名`
  ```sh
  ./rust-mysql-checker root 123456 127.0.0.1 3306 openapi_casbin
  ```
  `返回结果 会打印mysql版本号,以及库所有的表名`
  ```
  将获取MySQL版本号
  MySQL version: 8.0.30
  将获获取数据库: openapi_casbin 表数据
  table: casbin_rule
  ```   
#### rust-redis-checker
- 为何开发
  - 开发某次给我说在k8s pod内连不上redis,然后pod内又没有redis客户端,也无法安装navicat类的可视化工具,所以运维需要快速判断redis是否通畅,所以开发了此工具
- 提供版本
  - windows x86_64
    - 二进制文件
  - linux x86_64
    - 二进制文件
- 如何使用
  `./rust-redis-checker 密码 host 端口 库名`
  ```sh
  ./rust-redis-checker 123456 127.0.0.1 6379 4
  ```
  `返回结果 会先set一个40秒过期的测试key在你制定的库分区,然后在查询key的值`
  ```
  设置Redis Key: vincent_test_checker Value: 30 过期时间: 40 秒 DB: 4 成功
  查询到测试 key: vincent_test_checker value: 30  DB: 4 成功
  恭喜,您的Redis联通测试通过
  ```     
#### 如有疑问请联系作者
- E-Mail/QQ: 46603415@qq.com

