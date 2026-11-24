# 个人考公软件

这个项目用于开发一套自己使用的考公备考软件。项目技能指导 Codex 做产品设计、编码和验证。用户在软件里完成规划、练习、复盘和复测。

| 开发任务 | 项目技能 |
| --- | --- |
| 前端对话的开发与原理学习 | [exam-frontend-dev](skills/exam-frontend-dev/SKILL.md) |
| 后端对话的开发与原理学习 | [exam-backend-dev](skills/exam-backend-dev/SKILL.md) |
| 软件内 Agent 开发与 Python 原理学习 | [exam-agent-dev](skills/exam-agent-dev/SKILL.md) |
| 交付功能、看懂本次新改的代码 | [exam-code-walkthrough](skills/exam-code-walkthrough/SKILL.md) |
| 梳理需求、划分版本、决定优先级 | [exam-product-design](skills/exam-product-design/SKILL.md) |
| 实现阶段目标、周重点、每日任务和进度 | [exam-plan-dev](skills/exam-plan-dev/SKILL.md) |
| 实现题库、练习、计时、交卷和作答记录 | [exam-attempt-dev](skills/exam-attempt-dev/SKILL.md) |
| 实现 AI 复盘、错因、复测和提分统计 | [exam-feedback-dev](skills/exam-feedback-dev/SKILL.md) |
| 搭建软件、实现跨模块流程或验证集成 | [exam-system-dev](skills/exam-system-dev/SKILL.md) |

按当前开发任务读取对应技能。涉及多模块时，以用户实际使用的路径串联并验收。

## 开发原则

1. 前端、后端开发由不同的对话负责，分别读取对应技能。前端负责页面、交互和前端状态，后端负责接口、持久化和业务实现。两端交付功能时都用代码导读技能，帮助用户看懂本次改动和验证使用结果。
2. 围绕「阶段目标 → 周重点 → 今日任务 → 作答 → 复盘 → 新题复测」做轻量迭代。每次实现能在软件里体验的一小段流程，按需要引入技术。
3. 跨端任务先在共享需求台账写清接口输入、输出、状态及验证方式。两端对话在各自职责内实现，接口变更同步到同一条需求。涉及两端的功能以实际使用流程验收。
4. 用户提出或修正产品需求、开发原则或使用偏好时，在当轮更新 [需求台账](REQUIREMENTS.md)。保留尚未明确的事项，区分用户确认与方案建议。按角色接手前查看相关条目，交付后更新状态和验证证据。
5. 开发功能前先评估 GitHub 上可复用的实现，按许可证、接入成本和实际使用流程判断。能直接用或少量适配就复用，找不到适用实现再开发缺口。
6. 以自用体验为准，优先沿用现有结构和代码，保持职责清楚、目录紧凑。实际使用中的界面、接口和协同问题回写需求台账，按可复现的场景迭代。
