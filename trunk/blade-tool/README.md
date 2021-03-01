 <p align="center">
  <img src="https://img.shields.io/badge/license-LGPL%20v3-blue.svg" alt="Build Status">
   <img src="https://img.shields.io/badge/Spring%20Cloud-2020-blue.svg" alt="Coverage Status">
   <img src="https://img.shields.io/badge/Spring%20Boot-2.4.2-blue.svg" alt="Downloads">
 </p>  

## SpringBlade微服务开发平台
* 采用前后端分离的模式，前端开源两个框架：[Sword](https://gitee.com/smallc/Sword) (基于 React、Ant Design)、[Saber](https://gitee.com/smallc/Saber) (基于 Vue、Element-UI)
* 后端采用SpringCloud全家桶，并同时对其基础组件做了高度的封装，单独开源出一个框架：[BladeTool](https://github.com/chillzhuang/blade-tool)
* [BladeTool](https://github.com/chillzhuang/blade-tool)已推送至Maven中央库，直接引入即可，减少了工程的臃肿，也可更注重于业务开发
* 集成Sentinel从流量控制、熔断降级、系统负载等多个维度保护服务的稳定性。
* 注册中心、配置中心选型Nacos，为工程瘦身的同时加强各模块之间的联动。
* 使用Traefik进行反向代理，监听后台变化自动化应用新的配置文件。
* 极简封装了多租户底层，用更少的代码换来拓展性更强的SaaS多租户系统。
* 借鉴OAuth2，实现了多终端认证系统，可控制子系统的token权限互相隔离。
* 借鉴Security，封装了Secure模块，采用JWT做Token认证，可拓展集成Redis等细颗粒度控制方案。
* 稳定生产了一年，经历了从 Camden -> Hoxton -> 2020 的技术架构，也经历了从fat jar -> docker -> k8s + jenkins的部署架构
* 项目分包明确，规范微服务的开发模式，使包与包之间的分工清晰。

## 架构图
<img src="https://gitee.com/smallc/SpringBlade/raw/master/pic/springblade-framework.png"/>

## 工程结构
``` 
blade-tool
├── blade-core-boot -- 业务包综合模块
├── blade-core-cloud -- cloud封装模块
├── blade-core-develop -- 代码生成封装模块
├── blade-core-launch -- 基础启动模块
├── blade-core-log -- 日志封装模块 
├── blade-core-mybatis -- mybatis拓展封装模块 
├── blade-core-oss -- 对象存储封装模块 
├── blade-core-secure -- 安全模块 
├── blade-core-swagger -- swagger拓展封装模块 
├── blade-core-test -- 单元测试封装模块 
├── blade-core-tool -- 单元测试封装模块 
└── blade-core-transaction -- 分布式事物封装模块 
```
