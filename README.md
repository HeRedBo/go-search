# go-search

海量数据高并发场景，构建Go+ES8企业级搜索微服务课程商城系统 项目指引 

## 项目简介
海量数据高并发场景，构建`Go+ES8`企业级搜索微服务课程商城系统基于当前流行技术组合的前后端商城管理系统，
基于 `Golang` `微服务架构`自主研发的现代化电商平台，核心创新在于深度集成 `Elasticsearch 8` 构建`高性能` `企业级搜索引擎`，实现商品、订单数据的毫秒级精准检索、复杂聚合分析与近实时同步(增量/全量)。
系统采用前后端完全分离设计 (`Vue.js` 前端)，后端通过 `Kafka` 高并发数据管道解耦核心业务与搜索索引构建/同步流程，确保数据最终一致性。利用 `Docker` 容器化实现服务快速部署、弹性伸缩与开发-生产环境一致性。
## 项目亮点：
**架构先进性：** 严格遵循微服务设计原则，服务边界清晰 (核心业务、搜索API、索引调度、消费者服务)，具备高内聚、低耦合、独立部署能力。
**搜索驱动业务：** ES8 不仅用于搜索，更作为核心数据视图，支撑商品展示、订单管理、数据分析等关键场景。
**工程化典范：** 采用 Go 社区推崇的 `project-layout` 标准结构，显著提升代码可维护性与团队协作效率。
**基础设施即代码：** 所有中间件 (`Redis`, `MySQL`, `Kafka`, `MongoDB`) 及核心服务均通过 Docker Compose管理。

## 项目地址说明 
| 项目地址 | 项目说明 | 其他 |
| --- | --- | --- |
|  https://github.com/HeRedBo/pkg | 核心基础设施库 - 对常用中间件 (`MySQL`, `Redis`, `Elasticsearch`, `Kafka`, `MongoDB`,` HTTP Client`) 及关键组件 (`Logger`,` Routine Pool`,`Shutdown`) 进行了高度抽象、统一封装与最佳实践集成，大幅提升各微服务开发效率、代码规范性与健壮性。  |  |
| https://github.com/HeRedBo/shop-main | 核心业务微服务 - 基于 `Gin` + `Gorm` + `JWT` 实现商城核心后端API (用户、商品、订单、支付等)，集成 `pkg` 库操作各类中间件 |  |
| https://github.com/HeRedBo/shop-search-api | 搜索API微服务 - 提供基于 ES8 的高性能、可扩展搜索接口 (Gin)，供前端调用。 |  |
| https://github.com/HeRedBo/shop-schedule |  索引调度服务 - 负责管理 ES 索引的生命周期（创建、`Mapping`定义、`Alias` 切换）。 |  |
|https://github.com/HeRedBo/order-consumer https://github.com/HeRedBo/product-consumer  | 数据同步消费者 - 基于 `Kafka` 监听业务变更事件，高效、可靠地将订单/商品数据近实时同步到 `ES8`，保证搜索数据新实时更新和同步 |  |
|  https://github.com/HeRedBo/shop-admin | Vue 管理后台 - 提供系统管理、商品管理、订单管理、数据看板等功能。 |  |
|  https://github.com/HeRedBo/shop-web | Vue 商城前端 - 面向用户的商品浏览、搜索、下单界面。 |  |
