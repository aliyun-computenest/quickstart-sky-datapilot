# Sky DataPilot 服务实例部署文档

## 概述


`九象（Sky DataPilot）是一款专注于开源大数据平台的数据化运维与效能提升专家产品，致力于以数据化、智能化的方式为大数据平台提供运维产品服务，帮助客户提升平台的稳定性和效能。Sky DataPilot集成了贝联珠贯独特的大数据任务优化技术，在保证任务稳定运行的前提下，自动化的提升任务执行效率，提升集群使用效率或降低成本30%以上。` 
`本文向您介绍如何开通计算巢上的 Sky DataPilot 服务，以及部署流程和使用说明。`


## 计费说明

`本产品在云市场平台提供的版本为社区版本，产品本身免费使用（因云市场上架商品价格必须大于1元，为通过云市场商品上架审核故将商品设置为2元），但需要付费购买计算资源使用权限。`

```
Sky DataPilot 在计算巢上的费用主要涉及：

- 所选vCPU与内存规格
- 系统盘类型及容量
- 数据盘类型及容量

计费方式包括：

- 按量付费（小时）
- 包年包月

预估费用在创建实例时可实时看到。

```

## 部署架构

![部署架构](./pic/部署架构.PNG)

## RAM账号所需权限

`Sky DataPilot 服务实例部署需要使用RAM账号，请确保RAM账号具有以下权限：`


| 权限策略名称 | 备注 |
| --- | --- |
| AliyunECSFullAccess | 管理云服务器服务（ECS）的权限 |
| AliyunVPCFullAccess | 管理虚拟私有云（VPC）的权限 |


## 部署流程

### 部署步骤

1. 获取部署链接后，进入服务实例部署页面，根据页面提示，填写参数完成部署
2. 根据需要选择 ecs 规格、数据盘类型、数据盘大小
![机型及磁盘规格选择](./pic/机型及磁盘规格选择.png)
   磁盘规格参考：[磁盘规格](https://lccomputing.feishu.cn/wiki/wikcnbq6LHvAMZMhDP63GwfxOnb?fromScene=spaceOverview)
3. 选择 VPC、交换机（注意：网络选择要求部署服务的节点与大数据集群网络能够正常通信）
![ VPC及交换机选择](./pic/vpc选择.png)

### 使用说明
1. 部署完成后，即可通过公网IP或ECS实例的内网IP访问 Sky DataPilot 服务。
2. 登录 Sky DataPilot 服务后，页面会自动跳转到 License 注册页面，请先免费申请[License申请](https://lccomputing.feishu.cn/share/base/form/shrcnFfuxDLeWVSVaB0exsIDYtc)，按照页面提示完成 License 注册。
3. 完成 License 注册后，即可使用 Sky DataPilot 服务，需要在页面进行一些基础配置，参考[配置流程](https://lccomputing.feishu.cn/wiki/wikcngElLRoiBHoxlvsGtN4SlYe?fromScene=spaceOverview)。
4. 服务端配置完成后，需要部署客户端 hook 程序（如果大数据任务引擎是 spark 或者 tez 时需要部署），流程参考[hook部署](https://lccomputing.feishu.cn/wiki/wikcnbq6LHvAMZMhDP63GwfxOnb?fromScene=spaceOverview)。

## 联系我们

欢迎访问贝联珠贯官网（[https://www.lccomputing.com/](https://www.lccomputing.com/)）了解更多信息。

扫码关注微信公众号，技术博客、活动通知不容错过：

![微信公众号](./pic/微信公众号.png)