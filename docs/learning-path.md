# mall 后端学习路线（基于本仓库模块）

## 阶段一：工程骨架与公共能力
1. `mall-common` —— 统一返回体、全局异常、工具类，是所有模块的地基
2. `mall-mbg` —— 用 MBG 把表生成 Entity / Mapper，理解"表 → 代码"的自动化

## 阶段二：安全
3. `mall-security` —— Spring Security + JWT：登录颁发 token、拦截器校验、注解控制权限

## 阶段三：业务 API
4. `mall-admin` —— 后台管理：商品 / 订单 / 用户，重点看 controller→service→dao 分层
5. `mall-portal` —— 前台商城：会员 / 购物车 / 下单流程

## 阶段四：检索
6. `mall-search` —— 商品检索接入 Elasticsearch：索引构建 + 查询

## 建议
- 每个模块先读 `pom.xml` 看依赖，再读 `*Application` 启动类；
- 用 `mall-demo` 做最小跑通实验，再回看大模块；
- 画一张"请求从 controller 到数据库"的时序图，比抄代码收获更大。
