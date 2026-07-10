# Research Notebook / Excalidraw 视觉规则

## 视觉定位

这种图不是论文正式 Figure，而是“研究者白板笔记”：

- 让人 10 秒内看出论文主线。
- 比表格更有传播力。
- 比卡通教学更适合论文、系统设计和工程观点。

## 默认风格

- 3:4 竖版，小红书优先。
- 白底。
- 黑色手绘线条，轻微不规则。
- 少量红蓝橙绿强调。
- Excalidraw 风格方框、箭头、便签、圈注、下划线。
- Research Notebook 气质：聪明、清爽、像读论文时画在白板上的图。

## 色彩语义

```text
红色：问题、风险、限制、失败点
蓝色：方法、系统结构、技术机制
绿色：结果、收益、验证通过
黄色/橙色：核心 insight、创新、takeaway
紫色：可选，用于元层级、框架、范式变化
```

## 文字策略

生图模型容易生成错误中文，因此：

- 图内优先用英文短标签：`Paper Map`、`Problem`、`Method`、`Result`、`Risks`、`Insight`。
- 中文长句作为 overlay 文案，不直接交给生图模型。
- 论文题目、作者、年份、指标、公式和引用必须后期校对。
- 如果必须在图中生成中文，控制在 2-8 个汉字。

## 推荐画面

### Paper Map

一张总结构图，按纵向脊柱串起：

```text
One-line -> Problem -> Method -> Result -> Innovation -> Risks -> Insight
```

### Core Idea

一张核心机制图，展示论文最重要的转变：

```text
Before -> Gap -> Key Idea -> After
```

### Risk / Limitation

用红色警示便签、检查点、断裂链条或天平表示边界，不要假装论文没有局限。

## 避免

- 密密麻麻的论文表格。
- 纯 corporate slide 风。
- 大段中文、长英文段落。
- 过度拟人化，导致不像论文阅读。
- 没有主线的模块堆砌。
