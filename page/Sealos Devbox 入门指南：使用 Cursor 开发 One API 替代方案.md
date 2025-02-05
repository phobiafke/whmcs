# Sealos Devbox 入门指南：使用 Cursor 开发 One API 替代方案

随着技术的进步和人工智能的崛起，许多原本需要团队协作才能完成的任务如今可以通过自动化和智能化工具轻松实现。这不仅提升了开发者的工作效率，也让我们能够专注于更核心的技术挑战。

在本教程中，我们将通过一个实际的业务案例，展示如何利用 **Sealos Devbox** 和 **Cursor** 从头开发一个生产级别的应用，替代传统 **One API** 的功能。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

## 为什么选择 Sealos Devbox？

Sealos 平台上的许多应用都是通过 **Cursor + Go + Next.js** 开发的。我们的开发环境直接使用 **Sealos Devbox**，并通过它实现一键部署。这种开发模式极大地提升了团队的工作效率，**自动化工具和 AI 技术** 让开发者能够专注于业务逻辑。

![Sealos Devbox](https://bbtdd.com/img/45653111114943.webp)

以 **Sealos AI Proxy** 为例，这是一个典型的前后端分离架构的应用，主要由两个部分组成：

1. **基于 Next.js 的前端应用和 BFF 层**：负责用户鉴权，并将已验证的请求转发给后端服务。
2. **基于 Golang 的后端服务**：处理核心业务逻辑，包括 token 存储、日志记录和请求转发。

![AI Proxy 架构](https://bbtdd.com/img/493477123.webp)

接下来，我们将详细介绍如何高效开发这样一个系统。

## Golang 后端开发

### 创建开发环境

首先在 **Sealos Cloud** 中打开 **Devbox** 应用，创建一个新项目，选择 Go 作为运行环境，版本为 1.23。

![创建 Devbox 项目](https://bbtdd.com/img/98143786390938.webp)

**Devbox** 提供了以下实用功能：

- **灵活的资源配置**：根据项目需求调整 CPU 和内存，平衡性能与成本。
- **一键启用 HTTPS**：自动分配安全域名，无需手动配置 SSL 证书。
- **全自动域名管理**：域名配置由系统处理，开发者专注于代码。

创建完成后，几秒钟即可启动开发环境。使用 **Cursor** 连接开发环境，首次打开时会提示安装 **Devbox 插件**，安装后即可自动连接。

![Cursor 连接 Devbox](https://bbtdd.com/img/2322140573588566.webp)

### 导入项目到 Cursor

首先 Fork **Sealos 源码** 到自己的仓库，然后将其克隆到 **Devbox** 开发环境：

![Fork 源码](https://bbtdd.com/img/72216281466.webp)

### 测试环境开发

在 **Cursor** 中切换到 **Database** 标签页，打开 **Sealos 的数据库应用**，创建 PostgreSQL 和 Redis 实例。

![创建数据库实例](https://bbtdd.com/img/52409774834.webp)

回到 **Cursor**，刷新即可看到刚创建的数据库实例，复制连接信息并在终端中启动服务：

bash
export ADMIN_KEY=sealos-admin
export SQL_DSN=<复制的pgsql连接串>/postgres
export REDIS_CONN_STRING=<复制的redis连接串>
go run . --port 8080


启动成功后，使用 `curl` 进行测试：

bash
curl https://mmznjndvzdrv.sealoshzh.site/api/status -H "Authorization: sealos-admin"


### 优化数据库设计

在开发过程中，我们发现 **Group** 和 **Token** 之间的外键约束增加了系统维护的复杂度。为了简化这一关系，可以将外键约束改为程序层面的显式调用。

通过 **Cursor 的 Chat 功能**，让 AI 生成代码，优化数据库设计。这种方式能够在事务内完成相关操作，确保数据一致性。

### 上线到生产环境

在 **Cursor** 中设置启动命令，然后进入 **Devbox 发布页面** 发布版本。部署完成后，复制公网地址进行测试：

bash
curl https://jpesudzryuhp.sealosbja.site/api/tokens/ -H "Authorization: sealos-admin"


## Next.js 前端开发

### 前端项目搭建

在 **Devbox** 中创建一个 **Node.js** 环境，版本选择 20，端口改为 3000。克隆 Fork 的 **Sealos 仓库**，切换到 `sealos/frontend` 目录，安装依赖并构建项目。

### 对接后端环境

在项目根目录创建 `.env` 文件，配置环境变量以对接后端服务。运行 `pnpm dev` 启动开发服务器。

## 总结

**Sealos AI Proxy** 项目采用了 **Next.js App Router** 架构，通过分层设计让 **Golang 后端** 专注于核心业务逻辑。这种开发模式不仅高效，还能显著提高代码的可维护性。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)