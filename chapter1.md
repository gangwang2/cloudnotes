---
permalink: micro1.html
---

# Microservices

Micro service is an architecture pattern for large scale and complex application in the cloud era.

http://microservices.io/patterns/microservices.html



## Microservice 基础架构内容

1. 服务框架. RPC vs. REST; 二进制 vs 文本序列化; TCP vs HTTP; 契约 vs 代码优先; 客户端自动生成; 跨语言互操作.
2. 运行时支撑服务. 服务网关; 服务注册发现; 负载均衡; 配置中心.
3. 服务安全. Oauth; jwt; IAM.
4. 后台服务. 消息系统; 分布式数据访问层; 任务调度; 缓存管理.
5. 服务容错. 超时; 熔断; 隔离; 限流; 降级.
6. 服务监控. 日志监控; 调用链监控; Metrics监控; 告警通知; 健康检查.
7. 服务部署平台. 发布机制\(蓝绿; 金丝雀; 灰度\); 容器调度平台; 发布系统; 镜像治理; 租户资源治理; 发布流水线.

## 微服务架构体系

将上述架构基本内容组织成体系, 表现为.

1. 接入层. 外部nginx, 内部nginx等.
2. 业务服务层. 基础服务和聚合服务.
3. 支撑服务. 服务的注册与发现, 集中配置; 容错; 授权认证; 日志聚合; 监控警告; 后台服务.
4. 平台服务. 发布系统; 集群资源调度; 镜像治理; IAM.
5. 基础设施层. compute, network, storage, NOC监控, 安全, IDC.

## 服务发布系统

1. 管理员把镜像push到镜像治理中心
2. 管理员从"租户资产治理中心"申请资源.
3. 管理员从"发布控制台"去"发布"服务.
4. "发布控制台"从"租户资产治理中心"查询发布规格.
5. "发布控制台"从"kubernetes"平台上启动服务实例.
6. "Kube云" 从"镜像治理中心"pull镜像.
7. "Kube云"向"服务治理注册中心"注册服务.
8. "发布控制台"向"服务治理注册中心"调拨流量.
9. "服务治理注册中心"向"网关"提供"服务发现"能力.
10. 当流量从"网关"进入后, 能从"服务治理注册中心"发现服务, 流量流向 Kube云.

## 持续交付流水线

1. Jenkins从GIT得到代码, 构建, 单元测试, 打镜像, 发布到测试环境; UAT环境和生产环境.
2. 在发布到生产环境时, 分三个批次执行. 蓝绿, 灰度发布. 

## 服务跟踪平台

| 特性 | CAT | zipkin | pinpoint |
| :--- | :--- | :--- | :--- |
| 一句话描述 | centralized application tracking | distributed tracing system. |  |
|  |  | [https://zipkin.io/](https://zipkin.io/) |  |
| 调用链可视化 | 有 | 有 | 有 |
| 报表 | 非常丰富 | 少 | 中等 |
| ServerMap | 简单依赖图 | 简单 | 好 |
| 埋点方式 | 侵入 | 侵入 | Java 字节码增强 |
| Heartbeat | 有 | 无 | 有 |
| Metric | 有 | 无 | 无 |
| Java/.Net client | 有 | 有 | Java |
| Dashboard 中文 | 好 | 无 | 无 |
| 社区 | 好. 作者在国内 | 好. 无中文社区 | 一般. 无中文社区 |
| 国内案例 | 携程 点评等 | 阿里 京东 |  |
| 源头 | eBay CAL - centralized application logging | Google Dapper 论文 | Google Dapper 论文 |

References

