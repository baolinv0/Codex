# Codex 使用技巧分类索引

建议把 Codex 经验分为 8 类。每一类解决不同问题，避免所有内容都堆成 prompt。

## 1. Setup / Environment
解决 Codex 如何进入工程、理解环境、运行代码。

典型内容：
- 仓库初始化
- 环境安装
- GPU / Docker / Conda
- 权限与外部工具
- 本地、云端、远程服务器协作

## 2. Context / Instructions
解决“如何让 Codex 正确理解项目”。

典型内容：
- AGENTS.md
- 项目约束
- 如何提供最小充分上下文
- 如何让 Codex 先读代码再修改
- 长任务的上下文组织

## 3. Workflow / Git
解决“Codex 如何完成一次完整工程任务”。

典型内容：
- branch 策略
- commit / PR
- feature / fix / refactor
- worktree
- 多任务并行
- 完成后的交付检查

**当前 GitHub branch 规范属于这一类。**

## 4. Coding / Implementation
解决“如何提高编码正确率”。

典型内容：
- 小步修改
- interface-first
- 先 baseline 后修改
- 避免无关重构
- config / data / model 分离

## 5. Testing / Debugging / Review
解决“如何证明代码真的能工作”。

典型内容：
- 单元测试
- smoke test
- regression
- reviewer agent
- diff review
- 错误定位
- CI

## 6. Research / Experiment
面向算法、科研项目。

典型内容：
- hypothesis → experiment → metric → decision
- 一个实验分支对应一个主要假设
- baseline 固定
- ablation
- 失败样本分析
- 实验可复现
- 自动科研闭环

## 7. Agent / Parallelism
解决复杂任务如何拆给多个 Agent。

典型内容：
- build / review 分离
- 并行子任务
- dependency graph
- 多 Agent 汇总
- reviewer gate
- human approval boundary

## 8. Recipes / Cases
保存经过验证、可以复用的实战模式。

例如：
- “让 Codex 接手陌生 GitHub 工程”
- “实现论文并复现实验”
- “修一个训练 pipeline”
- “完成代码后自动创建 branch + PR”
- “科研 experiment branch 的标准流程”

---

## 内容类型

除主题分类外，每篇内容还应标记类型：

| 类型 | 含义 |
|---|---|
| Rule | 必须遵守 |
| Workflow | 标准操作流程 |
| Technique | 提高成功率的方法 |
| Template | 可复制模板 |
| Case | 实际案例与复盘 |

建议标题格式：

`[Rule] Never modify main directly`

`[Workflow] Research experiment branch`

`[Technique] Ask Codex to inspect before editing`

`[Template] AGENTS branch policy`

`[Case] modular_neural_isp AE-aware TM`
