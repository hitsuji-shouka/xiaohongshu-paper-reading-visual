# xiaohongshu-paper-reading-visual

把论文、PDF、arXiv 链接、研究笔记或技术长文做成小红书 Research Notebook / Excalidraw 风格论文阅读分享图的 Codex Skill。

## 适合什么

适合把一篇论文快速压缩成可以分享、收藏和复习的视觉总结，例如：

- Loop Engineering
- Agent 系统论文
- LLM / RAG / Tool Calling 论文
- CV / MICCAI / NeurIPS / ICLR 论文
- 系统设计类技术长文
- 工程实践总结

这个 Skill 的重点不是生成论文正式 Figure，而是生成“读论文时快速抓住主线”的分享图。

## 核心结构

每篇论文默认先拆成 7 步：

```text
一句话总结
解决的问题
核心方法
关键结果
最大创新
主要局限
启发
```

## 默认输出

- 论文 7 步结构化总结
- 小红书标题选项
- 1-3 页快速分享结构，或 6-8 页完整解读结构
- Research Notebook / Excalidraw-style 生图提示词
- 中文 overlay 文案建议
- 小红书正文与标签
- 与配图同目录的 `xiaohongshu-copy.md`
- 论文事实与视觉 QA 检查

## 视觉风格

默认采用 Research Notebook / Excalidraw 风格：

- 3:4 竖版
- 白底
- 黑色手绘线条
- 便签、箭头、圈注、下划线
- 少量红蓝橙绿强调
- 英文短标签可以进入生图
- 中文长句、指标、公式、引用和论文标题优先后期排版

## 输出文件

每次成品会把所有 PNG 和可直接发布的文案放进同一个主题目录。文案固定保存为 `xiaohongshu-copy.md`，包含标题、备选标题、正文简介、标签、页数、比例和检查结果。

## 安装

```bash
mkdir -p ~/.agents/skills
cp -R xiaohongshu-paper-reading-visual ~/.agents/skills/
```

也可以放到项目级：

```text
.agents/skills/xiaohongshu-paper-reading-visual/
```

## 示例

```text
$xiaohongshu-paper-reading-visual
把 Loop Engineering 这篇文章做成 1-3 页小红书 Research Notebook 分享图。
```

## 目录结构

```text
xiaohongshu-paper-reading-visual/
├── SKILL.md
├── README.md
├── LICENSE
├── NOTICE.md
├── agents/
│   └── openai.yaml
└── references/
    ├── paper-summary-schema.md
    ├── research-notebook-style.md
    ├── xiaohongshu-paper-carousel.md
    ├── loop-engineering-example.md
    ├── qa-checklist.md
    ├── visual-style.md
    ├── xiaohongshu-layout.md
    └── attribution.md
```

## 署名

本 Skill 的教学视觉方法继承自本项目共享规范，并参考 `helloianneo/ian-xiaohei-illustrations` 的方法论。论文阅读图本身默认采用 Research Notebook / Excalidraw-style，不直接复刻 Ian 原始示例图。
