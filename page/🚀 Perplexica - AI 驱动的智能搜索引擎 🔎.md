# 🚀 Perplexica - AI 驱动的智能搜索引擎 🔎

## 目录

- [概述](#概述)
- [核心功能](#核心功能)
- [安装指南](#安装指南)
  - [使用 Docker 安装（推荐）](#使用-docker-安装推荐)
  - [非 Docker 安装](#非-docker-安装)
- [故障排除](#故障排除)
- [作为搜索引擎使用](#作为搜索引擎使用)
- [API 集成](#api-集成)
- [支持我们](#支持我们)

## 概述

Perplexica 是一款开源 AI 驱动的智能搜索引擎，致力于深入挖掘互联网以提供精准答案。受 Perplexity AI 启发，它不仅是传统网页搜索的替代品，还能理解您的需求，并通过先进的机器学习算法（如相似性搜索和嵌入技术）优化结果，同时提供清晰的来源引用。

借助 SearXNG 技术，Perplexica 始终确保您获取最新信息的同时，保护您的隐私。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

## 核心功能

- **本地 LLM 支持**：通过 Ollama，您可以使用诸如 Llama3 和 Mixtral 等本地大语言模型。
- **两种主要模式**：
  - **Copilot 模式**（开发中）：通过生成多组查询，挖掘更多相关互联网资源。
  - **普通模式**：直接处理查询并执行网页搜索。
- **专注模式**：6 种特定场景的搜索模式：
  - **全模式**：在整个互联网中寻找最佳结果。
  - **写作助手模式**：专注于无需联网的写作任务。
  - **学术搜索模式**：查找学术论文，适合研究型用户。
  - **YouTube 搜索模式**：根据查询定位相关视频。
  - **Wolfram Alpha 搜索模式**：解决需要计算或数据分析的查询。
  - **Reddit 搜索模式**：搜索 Reddit 中的讨论和观点。
- **实时信息获取**：无需担心信息过时，Perplexica 使用 SearXNG 确保最新结果。
- **API 支持**：轻松将 Perplexica 集成到您的应用中。

## 安装指南

### 使用 Docker 安装（推荐）

1. 确保 Docker 已在系统中安装并运行。
2. 克隆 Perplexica 仓库：
   bash
   git clone https://github.com/ItzCrazyKns/Perplexica.git
   
3. 进入项目目录。
4. 将 `sample.config.toml` 重命名为 `config.toml`，并根据需要填写相关字段。
5. 运行以下命令启动：
   bash
   docker compose up -d
   
6. 访问 `http://localhost:3000` 开始使用。

### 非 Docker 安装

1. 安装 SearXNG 并启用 `JSON` 格式支持。
2. 克隆仓库并配置 `config.toml` 文件。
3. 在 `ui` 文件夹中配置 `.env` 文件。
4. 安装依赖并构建项目：
   bash
   npm i && npm run build
   
5. 启动前后端服务。

## 故障排除

### Ollama 连接错误

1. 检查 API URL 设置。
2. 根据操作系统调整 URL：
   - **Windows/Mac**：`http://host.docker.internal:11434`
   - **Linux**：`http://<private_ip_of_host>:11434`
3. 确保防火墙未阻止相关端口。

## 作为搜索引擎使用

将 Perplexica 添加为浏览器默认搜索引擎：
1. 打开浏览器设置。
2. 进入“搜索引擎”选项。
3. 添加新搜索引擎，URL 为 `http://localhost:3000/?q=%s`。

## API 集成

Perplexica 提供强大的 API，支持开发者将其功能集成到自己的应用中。查看 [API 文档](https://github.com/ItzCrazyKns/Perplexica/tree/master/docs/API/SEARCH.md) 获取更多信息。

## 支持我们

如果您觉得 Perplexica 对您有所帮助，请在 GitHub 上为我们点亮 ⭐️。您的支持激励我们不断完善功能，推动项目发展。我们同样接受捐赠，所有贡献都将直接用于项目维护与优化。

---

Perplexica 致力于让每个人都能轻松使用 AI 和大语言模型。如果您有任何建议或遇到问题，请通过 GitHub Issues 或 Discord 与我们联系。感谢您的支持与反馈！