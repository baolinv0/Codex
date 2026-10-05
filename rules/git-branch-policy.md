# Git Branch Policy

**Type:** Rule  
**Scope:** Codex coding projects

## 目的

保证 Codex 完成代码任务后，修改具有明确来源、可 review、可回滚，并且科研实验之间不会相互污染。

## Branch 类型

```text
feat/<task>       已验证、准备产品化的新能力
exp/<task>        科研假设、探索性实验
fix/<task>        Bug 修复
refactor/<task>   不改变目标行为的结构调整
data/<task>       数据集或数据生成 pipeline
eval/<task>       评测、benchmark、IQA、metrics
docs/<task>       文档
```

## 强制规则

1. **禁止直接修改 main。**
2. 开始代码修改前必须确认当前 branch。
3. 默认从最新 `main` 创建 task-specific branch。
4. 一个 branch 只对应一个主要工程目标或科研假设。
5. 不允许把无关修改混入当前 branch。
6. 完成后必须运行与修改相关的测试。
7. Codex 必须汇报：
   - branch name
   - base commit
   - changed files
   - tests executed
   - known failures / risks
8. Codex 可以 commit / push，但**不得自动 merge 到 main**，除非用户明确授权。

## 任务到 branch 的映射

| 任务 | branch |
|---|---|
| 新产品功能 | `feat/*` |
| 研究假设 | `exp/*` |
| 数据生成 | `data/*` |
| 评测系统 | `eval/*` |
| Bug | `fix/*` |
| 重构 | `refactor/*` |
| 文档 | `docs/*` |

## 科研项目附加规则

推荐：

```text
one branch ≈ one primary hypothesis
```

例如：

```text
exp/tm-ae-conditioning
exp/tm-semantic-guidance
exp/tm-lut-head
```

不要使用：

```text
exp/improve-tm
```

然后在同一个 branch 同时修改 AE、语义、Loss、数据、网络结构。

## 推荐执行流程

```text
inspect repository
      ↓
inspect current branch/status
      ↓
update main
      ↓
classify task
      ↓
create task branch
      ↓
implement
      ↓
test
      ↓
review diff
      ↓
commit/push
      ↓
report
      ↓
human decides merge
```
