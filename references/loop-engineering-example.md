# 示例：Loop Engineering

论文：

`Loop Engineering: The Anthropic Playbook for Designing Systems That Prompt Your Agents`

## 7 步总结

### 一句话总结

Loop Engineering 把人从“反复提示 Agent”的位置移出来，转去设计能发现、执行、验证、记忆并再次启动的循环系统。

### 解决的问题

Prompt、Context、Harness 都默认人还坐在键盘前，一次次启动 Agent。真正的瓶颈是：人仍然是循环里的时钟。

### 核心方法

把单次 Agent run 上移为 Loop。一个 loop turn 包含五个动作：

```text
Discovery -> Handoff -> Verification -> Persistence -> Scheduling
```

六个部件支撑它：

```text
Automations, Worktrees, Skills, Connectors, Sub-agents, Memory
```

### 关键结果

文章给出从个人 morning triage 到企业级流水线的实践案例，说明 loop 已经从概念进入工程实践。核心结论是：生成会越来越便宜，判断会变得稀缺。

### 最大创新

不是写一个更强的 Agent，而是把工作方式上移一层：从操作 Agent，变成设计能提示 Agent 的系统。

### 主要局限

Loop 会静默累积四种成本：

```text
Verification debt
Comprehension rot
Cognitive surrender
Token blowout
```

如果没有独立 evaluator 和 human checkpoint，loop 只是一个会自我点头的系统。

### 启发

未来工程师的价值会更集中在判断力：设边界、放检查点、抽样阅读、控制预算、能说“不”。

## 推荐两页结构

### 第 1 页：封面 / 核心概念

主题：

```text
Loop Engineering
Prompt -> Loop
Human stays judge
Can say NO
```

画面：

- 左侧：疲惫的人手动输入 prompts。
- 中间：五步循环。
- 右侧：工程师站在循环外设计系统。
- 中央检查点：Judge / Checkpoint 能说 NO。

### 第 2 页：Paper Map

纵向结构：

```text
One-line
Problem
Method
Result
Innovation
Risks
Insight
```

短标签：

```text
Prompt -> Loop
5 moves
Judgment is scarce
Stay the engineer
```

## 生图提示词重点

使用：

```text
Research Notebook / Excalidraw-inspired hand-drawn paper map,
vertical 3:4 Xiaohongshu carousel,
clean white background,
black sketchy ink lines,
soft pastel sticky-note blocks,
sparse red/blue/yellow/green accents,
short English labels only,
avoid long Chinese text.
```
