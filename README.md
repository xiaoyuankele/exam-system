# 个人考公软件

面向个人使用的考公备考系统，围绕计划、作答、AI 复盘和复测开发。

## 项目技能架构

前端与后端在各自对话中开发，共用需求和接口约定。Agent 在后端内运行。三类开发交付都使用代码导读技能，沿一次实际操作带用户找到关键代码并验证效果。

```mermaid
flowchart TB
    Entry["项目入口 · AGENTS.md"]
    Ledger["共享需求台账 · REQUIREMENTS.md"]
    subgraph Design["设计与集成"]
        Product["exam-product-design · 产品范围与验收"]
        System["exam-system-dev · 跨模块集成与联调"]
    end
    subgraph Dev["开发分工"]
        Front["exam-frontend-dev · 页面与交互"]
        Back["exam-backend-dev · 接口与数据"]
        Agent["exam-agent-dev · 模型调用与复盘"]
        Back -->|按需使用| Agent
    end
    subgraph Domain["共享业务规则"]
        Plan["exam-plan-dev · 计划与今日任务"]
        Attempt["exam-attempt-dev · 题库、配图与交卷"]
        Review["exam-feedback-dev · 复盘与复测"]
        Plan --> Attempt --> Review
    end
    Walk["新增 · exam-code-walkthrough<br/>实际操作 → 关键代码 → 自己验证"]

    Entry --> Product
    Entry --> System
    Product --> Ledger
    System --> Ledger
    Ledger --> Front
    Ledger --> Back
    Front --> Domain
    Back --> Domain
    Front ==>|前端交付| Walk
    Back ==>|后端交付| Walk
    Agent ==>|Agent 交付| Walk

    classDef added fill:#ede9fe,stroke:#6d28d9,stroke-width:3px,color:#25134d
    class Walk added
```

- [项目规则和技能入口](AGENTS.md)
- [需求台账和首版联调约定](REQUIREMENTS.md)
- [开发代码导读技能](skills/exam-code-walkthrough/SKILL.md)
