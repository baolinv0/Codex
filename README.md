# Codex Engineering Handbook

用于统一沉淀 Codex 的工程实践、工作流、规则、模板与案例。

> 本仓库不是零散 prompt 收藏夹。目标是把“如何稳定地让 Codex 完成工程任务”沉淀成可复用的工程规范。

## 内容分层

- **Rules**：Codex 必须遵守的硬规则，例如分支、测试、提交、禁止直接修改 main。
- **Workflows**：完成一类任务的标准流程，例如新功能开发、Bug 修复、代码 Review、科研实验。
- **Techniques**：提高效果的具体技巧，例如如何给上下文、如何拆任务、如何要求自检。
- **Templates**：可直接复制到项目中的 AGENTS.md、任务说明、实验记录、Review 模板。
- **Cases**：真实工程案例及复盘，记录什么有效、什么无效。

## 推荐目录

```text
Codex/
├── README.md
├── AGENTS.md
├── docs/
│   └── INDEX.md
├── rules/
│   └── git-branch-policy.md
├── workflows/
│   └── git-branching.md
├── techniques/
├── templates/
│   ├── AGENTS.branching.md
│   ├── TASK.md
│   └── EXPERIMENT.md
└── cases/
```

## 核心原则

1. Rule 与 Tip 分开：强约束不能埋在经验文章里。
2. Workflow 描述“步骤”，Template 提供“可复制文本”。
3. 一条技巧只解决一个明确问题。
4. 重要实践必须记录适用条件与失败边界。
5. 对代码工程默认采用 task-specific branch，不直接修改 main。

详细导航见 `docs/INDEX.md`。
