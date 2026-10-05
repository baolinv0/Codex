# Workflow: Codex 完成代码任务时如何管理 Branch

**Type:** Workflow

## Step 1 — 先分类任务

Codex 在写代码之前先判断：

```text
Research hypothesis       -> exp/
Production feature        -> feat/
Dataset generation        -> data/
Evaluation infrastructure -> eval/
Bug fix                   -> fix/
Refactoring               -> refactor/
Documentation             -> docs/
```

## Step 2 — 检查仓库状态

至少检查：

```bash
git status
git branch --show-current
git log -1 --oneline
```

如果存在用户未提交修改，不得覆盖或清理。

## Step 3 — 从正确 baseline 建 branch

默认：

```bash
git checkout main
git pull --ff-only origin main
git checkout -b <type>/<task-name>
```

如果任务明确要求基于已有实验 branch，则以指定 branch 为 base。

## Step 4 — 实现期间保持 branch scope

允许：
- 当前任务需要的代码
- 当前任务需要的测试
- 当前任务需要的配置/文档

避免：
- 顺手重构大量无关代码
- 修复与当前任务无关的问题
- 同时验证多个互相独立的科研假设

## Step 5 — 完成前 Gate

Codex 必须完成：

```text
[ ] implementation finished
[ ] relevant tests executed
[ ] diff reviewed
[ ] temporary debug code removed
[ ] config / path checked
[ ] known failures recorded
[ ] branch name still matches actual task
```

## Step 6 — 输出交付摘要

标准输出：

```text
Branch:
Base:
Objective:

Changed:
- ...

Validation:
- ...

Known issues:
- ...

Recommended next action:
- review / experiment / PR
```

## Step 7 — Merge 权限

默认停止在：

```text
branch pushed / PR ready
```

不要自动 merge。

只有用户明确说“合并”“merge PR”“合入 main”时才执行合并。
