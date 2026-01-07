# 商城后端学习实验室 (mall-learning-lab)

> 整理自 macrozheng 的 mall 项目（Apache-2.0）的学习型仓库。
> 保留原始 LICENSE 与署名（见 NOTICE）；本仓库仅做中文梳理、模块化拆分与本地化说明，便于系统学习 Spring Boot 电商后端。

## 项目定位

mall 是一套基于 Spring Boot + MyBatis 的电商后台后端示例，覆盖企业级 Spring 后端最常见的能力：统一返回、全局异常、权限安全（Spring Security + JWT）、MyBatis 代码生成、Elasticsearch 商品检索，以及前后台两套 API。

## 模块划分（Maven 多模块）

- `mall-common`：通用工具、常量、统一返回与异常基类、API 封装
- `mall-mbg`：MyBatis Generator 代码生成（表 → Entity / Mapper）
- `mall-security`：认证授权（注解 / 切面 / JWT 组件）
- `mall-demo`：最小可运行示例
- `mall-search`：基于 Elasticsearch 的商品检索
- `mall-admin`：后台管理 API（商品 / 订单 / 用户等）
- `mall-portal`：前台商城 API（会员 / 购物车 / 订单）

## 推荐学习顺序

1. `mall-common`：先理解统一返回与全局异常处理的设计；
2. `mall-security`：再看清 JWT 登录与鉴权链路；
3. `mall-mbg`：把数据库表变成可操作的 Mapper，是 CRUD 基石；
4. `mall-admin` / `mall-portal`：深入业务分层（controller / service / dao）；
5. `mall-search`：最后看检索如何接入 ES。

## 许可与署名

- 原始项目：macrozheng/mall，Apache-2.0。
- 本仓库保留原始 LICENSE；修改与整理说明见 NOTICE。
- 本仓库为学习整理用途，不声称原创代码，所有示例源码著作权归 macrozheng 所有。
