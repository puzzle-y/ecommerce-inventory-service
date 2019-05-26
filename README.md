# 本示例代码对应博客：
- [Spring Boot项目模板](https://www.jianshu.com/p/bd8136129dfb)

# 项目简介
本项目是ecommerce系统的库存（Inventory）子系统，用于管理产品库存。

# 技术选型
Spring Boot、Gradle、MySQL、Junit 5、Rest Assured、Docker

# 本地构建

在本地构建之前必须完成以下步骤：
- 命令行进入[`ecommerce-sample/devops`](https://github.com/e-commerce-sample/devops)项目的跟目录
- 运行`./start-nexus.sh`，用于启动Nexus
- 运行`./start-rabbitmq.sh`，用于启动RabbitMQ
- 命令行进入[`ecommerce-sample/common`](https://github.com/e-commerce-sample/common)项目的根目录
- 运行`./publish.sh`，该命令将推送公共的`common.jar`包到Nexus

|功能|命令|备注|
| --- | --- | --- |
|生成IntelliJ工程|`./idea.sh`|自动打开IntelliJ|
|本地运行|`./run.sh`|自动启动MySQL，监听5005调试端口|
|本地构建|`./local-build.sh`|启动启动MySQL，运行所有类型的自动化测试|
|停止MySQL|`./gradlew composeDown`|将清空所有数据|
|手动启动MySQL|`./gradlew composeUp`||

# 领域对象
|领域对象|中文名|业务功能|
| --- | --- | --- |
|Inventory|库存|表示某个Product的库存信息|

# 测试策略
|测试类型|代码目录|测试内容|
| --- | --- | --- |
|单元测试|`src/test/java`|包含核心领域模型（包含领域对象和Factory类）的测试|
|组件测试|`src/componentTest/java`|用于测试一些核心的组件级对象，比如Repository|
|API测试|`src/apiTest/java`|模拟客户端调用API|

# 技术架构
技术架构图

# 部署架构
部署架构图

# 外部依赖
列出项目所依赖的其他系统，比如订单系统依赖于会员系统。

# 环境信息
列出各个环境的访问方式，数据库连接等。

# 编码实践
列出常用的公共的编码实践方式。

# FAQ
常见问题列表

# 原则