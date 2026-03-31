# 从零构建 Code Agent：Claude Code 源码深度解析

> 一个面向开发者的系列教程，通过剖析 Claude Code 的真实源码，手把手教你理解并构建一个完整的 Code Agent。

## 这个教程讲什么？

Claude Code 是 Anthropic 推出的 AI 编程助手，它不只是一个聊天机器人——它是一个能读文件、写代码、执行命令、管理项目的**智能代理（Agent）**。本教程通过解读 Claude Code 的源码架构，带你从零理解构建一个 Code Agent 的全部关键技术。

## 教程目录

| 章节 | 标题 | 核心内容 |
|------|------|----------|
| [第一章](./01-architecture-overview.md) | **全局架构鸟瞰** | 什么是 Code Agent？Claude Code 的整体架构和核心设计理念 |
| [第二章](./02-cli-bootstrap.md) | **CLI 入口与启动流程** | 从命令行输入到系统就绪，一个 Agent 如何启动？ |
| [第三章](./03-tool-system.md) | **工具系统：Agent 的双手** | Tool 接口设计、权限控制、40+ 工具的注册与调度 |
| [第四章](./04-conversation-context.md) | **对话与上下文管理** | System Prompt 构建、CLAUDE.md、上下文窗口管理与自动压缩 |
| [第五章](./05-agent-loop.md) | **Agent 循环：大脑的运转** | QueryEngine、query loop、流式工具执行——Agent 的核心引擎 |
| [第六章](./06-hooks-permissions.md) | **权限系统与 Hooks** | 安全第一：工具权限检查、用户确认、自动模式判定 |
| [第七章](./07-extensions-mcp.md) | **插件、Skills 与 MCP** | 可扩展性设计：Skills 系统、Plugin 架构、MCP 协议集成 |
| [第八章](./08-build-your-own.md) | **实战：构建你自己的 Code Agent** | 综合实战，从零搭建一个简化版 Code Agent |

## 适合谁读？

- 对 AI Agent 技术架构感兴趣的开发者
- 想理解 Claude Code 内部实现原理的用户
- 正在构建或计划构建自己的 Code Agent 的工程师
- 对 LLM 应用开发（特别是 Tool Calling 和 Agent Loop）感兴趣的人

## 技术栈

教程涉及的核心技术：

- **TypeScript / Bun** — 主要编程语言和运行时
- **React / Ink** — 终端 UI 框架
- **Anthropic Claude API** — LLM 后端，流式响应和工具调用
- **MCP (Model Context Protocol)** — 工具扩展协议
- **Async Generators** — 流式数据管道的核心模式

## 源码版本

本教程基于 Claude Code **v2.1.88** 的源码进行分析。

## 许可

本教程内容采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 许可协议。
