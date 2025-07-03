# go-search

海量数据高并发场景，构建Go+ES8企业级搜索微服务课程商城系统 项目指引 


## 项目说明 


## 项目地址说明 


| 项目地址 | 项目说明 | 其他 |
| --- | --- | --- |
|  https://github.com/HeRedBo/pkg | 核心基础设施库 - 对常用中间件 (MySQL, Redis, Elasticsearch, Kafka, MongoDB, HTTP Client) 及关键组件 (Logger, Routine Pool, Graceful Shutdown) 进行了高度抽象、统一封装与最佳实践集成，大幅提升各微服务开发效率、代码规范性与健壮性。  |  |
| https://github.com/HeRedBo/shop-main | 核心业务微服务 - 基于 Gin + Gorm + JWT 实现商城核心后端API (用户、商品、订单、支付等)，集成 pkg 库操作各类中间件 |  |
| https://github.com/HeRedBo/shop-search-api | 搜索API微服务 - 提供基于 ES8 的高性能、可扩展搜索接口 (Gin)，供前端调用。 |  |
| https://github.com/HeRedBo/shop-schedule |  索引调度服务 - 负责管理 ES 索引的生命周期（创建、Mapping 定义、Alias 切换）。 |  |
|https://github.com/HeRedBo/order-consumer https://github.com/HeRedBo/product-consumer  | 数据同步消费者 - 基于 Kafka 监听业务变更事件，高效、可靠地将订单/商品数据近实时同步到 ES8，保证搜索数据新实时更新和同步 |  |
|  https://github.com/HeRedBo/shop-admin | Vue 管理后台 - 提供系统管理、商品管理、订单管理、数据看板等功能。 |  |
|  https://github.com/HeRedBo/shop-web | Vue 商城前端 - 面向用户的商品浏览、搜索、下单界面。 |  |
