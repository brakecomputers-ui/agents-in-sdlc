---
slug: zh-cn/real-world-development/cli
title: "GitHub Copilot CLI"
description: "学习 Copilot CLI 的模式、自定义配置、MCP 工具和拉取请求自动化，同时构建、验证并交付 Tailspin Toys 的两项变更。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

**[GitHub Copilot CLI][about-copilot-cli]** 将 GitHub Copilot 作为代理式编码助手带入终端。它可以探索代码库、生成代码、运行命令，并连接外部工具——全部通过命令行完成，无需切换到图形化编辑器即可保持工作流畅。

本工作坊将带你完成 Tailspin Toys 的一系列工作：

1. 在 GitHub Codespaces 中准备项目，安装 Copilot CLI 并熟悉其用法。
2. 添加星级评分，在浏览器中检查结果，并手动合并第一个拉取请求 (PR)。
3. 从筛选议题开始，在 Plan 模式中确定方案，在 Autopilot 模式中构建，然后在 Interactive 模式中审查。
4. 更新存储库说明，并将其应用于筛选工作。
5. 自定义现有的 `quality-checks` 技能，并使用它运行项目检查。
6. 添加 Playwright Model Context Protocol (MCP) 服务器，并在浏览器中探索筛选功能。
7. 创建质量保证 (QA) 自定义智能体，并用它审查需求、覆盖范围和验证证据。
8. 审查完整的筛选变更，并使用 Agent Merge 处理筛选 PR。
9. 探索用于管理上下文、模型、共享以及可选委托给云智能体的实用斜杠命令。

为保持工作坊重点清晰，你将创建两个 PR：一个用于星级评分，另一个用于筛选，并包含说明更新、技能更新、QA 配置和测试。筛选和质量工作共用一个对话和分支，让你在探索各项工具时可以继续已有工作。

## 练习

| 练习 | 主题 | 说明 |
|----------|-------|-------------|
| [0. 先决条件][ex0] | 设置 | 创建存储库和 Codespace |
| [1. 安装 Copilot CLI][ex1] | 安装 | 安装并验证 Copilot CLI，然后熟悉其用法 |
| [2. 添加星级评分：快速改进][ex2] | 首项变更 | 显示现有评分和 null 时的备用值，然后合并第一个 PR |
| [3. 智能体模式：Plan 和 Autopilot][ex3] | 智能体模式 | 根据议题规划功能，使用 Autopilot 构建，然后在 Interactive 模式中审查 |
| [4. 使用自定义说明引导 Copilot][ex4] | 上下文 | 查看并更新说明，然后将其应用于筛选工作 |
| [5. 自定义并使用质量检查技能][ex5] | 可重复检查 | 查看现有技能、更改报告格式并运行技能 |
| [6. 使用 Playwright MCP 验证功能][ex6] | 浏览器观察 | 在 CLI 中配置 MCP 并检查筛选行为 |
| [7. 创建和使用 QA 智能体][ex7] | 需求和覆盖范围 | 创建并选择专用配置，然后收集最终验证证据 |
| [8. 创建并合并功能 PR][ex8] | 审查和合并 | 审查完整变更、创建 PR 并使用 Agent Merge |
| [9. GitHub Copilot CLI 斜杠命令][ex9] | CLI 功能 | 探索上下文、模型、共享以及可选委托给云智能体 |
| [10. 总结与后续步骤][ex10] | 总结 | 回顾工作流、可复用的自定义配置和更多资源 |
| [可选：集成 Foundry][foundry] | 托管智能体 | 准备模型、部署基于目录的智能体并将其连接到网站 |

## 先决条件

参加本工作坊前，请确保已具备以下条件：

- [ ] 拥有 GitHub 账户，并已启用 **Copilot Student、Pro、Pro+、Business 或 Enterprise** 计划
- [ ] 有权创建存储库和 Codespace
- [ ] 对终端/命令行操作有基本了解

> [!TIP]
> 没有付费计划？已验证学生可通过 [GitHub Education][callout-student-plan-education] 免费使用 GitHub Copilot。**Copilot Student** 计划包含本工作坊所用的智能体、MCP、代码审查和 Copilot CLI 功能，因此可以完整完成所有路径。

> [!NOTE]
> 如果使用的是 Copilot Business 或 Copilot Enterprise，请确认管理员已启用 Copilot CLI。

[callout-student-plan-education]: https://github.com/education/students

## 开始

**[从练习 0：先决条件开始 →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
