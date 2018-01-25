---
date: 2018-01-26
---

# Cloud Landscape in 2018

应用, 是价值的直接表现. 平台, 是快速开发与部署应用的基础.

我们把云计算按层次划分为SaaS, PaaS, IaaS. 

数字化企业会使用很多SaaS服务: 销售管理Salesforce, HR系统Workday, 差旅报销Concur, 天猫和京东上开设销售店铺等.
SaaS软件服务商依托PaaS, IaaS来构建与运营SaaS服务. 微信, 支付宝, 王者荣耀等应用也是依托PaaS, IaaS来构建与运营.
大型的数字化企业还会开发很多供企业自身和合作伙伴使用的应用系统, 它们都可以依托PaaS, IaaS来构建与运营.

## Why Developer PaaS?

PaaS提供了应用软件运行所依赖的平台级软件服务环境, 如大数据平台, 数据库服务, 消息队列服务, 文件存储服务, 短信发送服务等具有共性的服务接口.
这些服务的重用, 极大地节省了开发工作和运维成本. 但是, 应用开发者仍然面临着开发环境, 测试环境, 线上环境等多个环境的挑战, 以及集成大量外部服务的挑战.

Developer PaaS则通过提供集成的平台环境, 进一步解放了应用开发者. Developer PaaS是践行Agile DevOps文化的企业应用开发者的得力助手, 它以托管代码库为起点, 通过持续集成, 持续测试和持续交付, 让代码以最高的效率和可靠的质量进入到线上环境. Developer PaaS打通了从代码到应用的全部环节.

## How to use Developer PaaS?


## Cloud Native Application

## Transforming

```
Service = Platform + Application
```

Platform加Application是构建服务的经典结构. Platform是基石级别的code, Application是利用Platform构建特定领域系统的形态. 

```
IaaS = Infrastructure PaaS + Infrastructure Application
```

IaaS的构建, 是在Infrastructure领域搭建Platform, 开发Infrastructure应用. 
IT用户可以通过Infrastructure Application来创建虚拟网络, 虚拟机, 数据存储设备等, 然后将软件部署到这些Infrastructure资源中运行. 在这种场景中,
IaaS比传统的计算资源申请方式而言, 有了极高的灵活性.从申请到可用的时间也更短.成本也更低.

让应用系统, 或者应用系统所在的应用平台, 通过 Infrastructure PaaS来申请和管理Infrastructure资源, 则比手工申请与管理具有更高的自动化. 对于大规模使用Infrastructure资源的客户而言, 这种自动化减少了管理成本, 且更好地服务于应用系统, 优势明显.

那么, 如何让应用系统能够自动管理Infrastructure的使用呢? Developer PaaS给出了答案.


```
Developer PaaS = Developer Platform + Application Platform
```


我们更准确的说, 都是将平台作为一种服务, Infrastructure platform-as-a-service,
Developer platform-as-a-service, and Cloud Application.

这里把SaaS解构了. 原先意义上的SaaS是具有多租户形态的应用. 而对于云计算应用平台提供商而言, 更多的是广义上的Cloud Application. 
基于 Developer platform-as-a-service, 构建 Cloud Application.  这些云应用程序, 更多的是面向企业自身需求的, 少数是SaaS -- 服务很多企业的.

通过把Platform的概念还原, 而把经典的PaaS定义为Developer PaaS, 把经典的IaaS定义为Infrastructure PaaS. 它准确表示了云计算行业的趋势. 
同时, 它也反应了Agile, DevOps等思想方法在云计算领域的运用.

相对于经典的IaaS而言, Infrastructure PaaS内涵了Infrastructure as Code的DevOps文化, 反应了Infrastructure代码化, 软件化的状态.
相比于经典的PaaS而言, Developer PaaS明确了软件技术平台所面向的用户对象Developer. 现在的PaaS就是Developer PaaS, 它的用户就是Developers.
