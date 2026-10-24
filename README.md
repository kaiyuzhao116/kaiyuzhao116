<!-- https://github.com/kaiyuzhao116/kaiyuzhao116/blob/main/README.md -->

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1e3c72,100:2a5298&height=140&section=header&text=Hi%2C%20I'm%20%E5%87%AF%E5%AE%87&fontSize=36&fontColor=ffffff" width="100%" />

## 👋 关于我

- 🎯 Java 后端 / 微服务方向，正在补底层原理
- 🔨 习惯把一个项目做成**完整闭环**：不只跑通，还讲清楚为什么这样设计
- 🌱 目前在深入：Netty 长连接、分布式消息可靠性、Dubbo 3

<p>
  <img src="https://img.shields.io/badge/Java-21-orange?logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring%20Cloud%20Alibaba-green?logo=spring&logoColor=white" />
  <img src="https://img.shields.io/badge/Dubbo-3-blue?logo=apache&logoColor=white" />
  <img src="https://img.shields.io/badge/Netty-4.x-green?logo=netty&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-CC0000?logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white" />
  <img src="https://img.shields.io/badge/Nacos-white" />
  <img src="https://img.shields.io/badge/Vue-3-4FC08D?logo=vuedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black" />
</p>

---

## 🚀 代表作：spring-cloud-im

> 一套**真正跑通的微服务即时通讯系统** —— 消息先落库、再推送；推送丢了靠拉取补偿；token 会过期但不会莫名掉线。

🔗 **在线体验**：http://82.157.185.69:8081 （账号 `admin` / `123456`，登录后左下角进管理后台）

| ⚡ 功能 | 🏗️ 架构 |
|---|---|
| 注册登录 / 加好友 / 实时消息 | api-gateway 验签 + Netty 接入层 |
| 历史分页 / 未读已读 / 断线补缺 | Dubbo 服务间调用 + MQ 广播推送 |
| 消息撤回 / 后台管理（踢人·禁用·改密） | 令牌桶 + 队列水位双层限流 |

**几个关键设计取舍**

- **先落库再推送**：ACK 只管"存住了没"，数据库才是真相，推送只是加速器
- **未读用减法**：`last_seq - last_read_seq`，不存计数，永远不会算错
- **踢人 = 收卡**：断连接之外还要作废凭证，否则刷新即复活
- **签发权只在 auth**：网关只验票，网关被攻破也伪造不了 token

👉 仓库地址：[spring-cloud-im](https://github.com/kaiyuzhao116/spring_cloud)（含 24 章设计文档、消息 36 步全链路拆解）

---

## 📦 其他项目

| 仓库 | 说明 |
|---|---|
| [social_school](https://github.com/kaiyuzhao116/social_school) | 校园社交 / 二手交易 |
| [instant](https://github.com/kaiyuzhao116/instant) | 即时通讯练习 |
| [strategy-chain-demo](https://github.com/kaiyuzhao116/strategy-chain-demo) | 责任链+策略+模板方法演示 |
| [mybatisplus_demo](https://github.com/kaiyuzhao116/mybatisplus_demo) | MyBatis-Plus 实践 |
| [tao-loop-demo](https://github.com/kaiyuzhao116/tao-loop-demo) | 循环练习 |

---

## 📊 GitHub 统计

<p>
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=kaiyuzhao116&show_icons=true&hide_border=true&count_private=true&include_all_commits=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kaiyuzhao116&layout=compact&hide_border=true&langs_count=6" />
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1e3c72,100:2a5298&height=100&section=footer" width="100%" />

