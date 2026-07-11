---
name: xiaohongshu-paper-reading-visual
description: Use when turning a paper, PDF, abstract, arXiv link, research note, or technical article into a Chinese Xiaohongshu paper-reading post, Research Notebook visual, Excalidraw-style paper map, paper explainer carousel, or shareable visual summary.
---

# 小红书论文阅读可视化 Skill

把论文或技术长文压缩成适合小红书分享的论文阅读图。目标不是复刻论文结构，而是让读者快速抓住：这篇文章讲什么、解决什么问题、方法是什么、为什么值得看、哪里要警惕、对自己有什么启发。

## 先读共享规范

制作前读取：

- `references/visual-style.md`
- `references/xiaohongshu-layout.md`
- `references/attribution.md`
- `references/xiaohongshu-copywriting.md`

默认视觉必须保持：3:4 竖版、白底、黑色手绘线稿、少量红蓝橙强调。可以使用读论文的人、工程师、研究员等角色帮助表达“理解、判断、检查、取舍”，但不要让角色抢走论文结构本身。

## 默认输出

除非用户只要求某个阶段，输出：

1. 论文 7 步结构化总结
2. 1 个最终小红书标题，另附 2 个备选标题
3. 1-3 页短分享结构，或 6-8 页完整解读结构
4. 每页已生成的 Research Notebook / Excalidraw-style 3:4 配图
5. 中文 overlay 文案建议
6. 简洁正文和标签
7. 技术准确性与视觉 QA 报告

## 直接成品交付

除非用户明确只要论文总结、脚本、分镜或提示词，否则必须直接完成可发布交付：

1. 必须调用内置 `image_gen`，先生成一张 Paper Map 总览，再生成用户要求的 1-3 张短分享图或 6-8 张完整解读图。
2. 所有配图必须是独立的 3:4 竖版图；不要只给 Research Notebook / Excalidraw-style 的提示词。
3. 生成后直接展示配图，再给出标题、简洁正文和 5-10 个精准标签。
4. 论文题目、中文长句、公式、引用和精确实验数字作为准确 overlay 文案提供，不依赖生图模型生成长文字。
5. 不得只输出分镜或提示词。只有 `image_gen` 不可用时，才说明原因并把每页完整提示词作为降级交付。

## 严格 3:4 成品检查

3:4 是硬性发布规格，不是生图提示词里的软性建议：

1. 每页提示词必须明确写 `3:4 vertical portrait` 和 `1080 × 1440`。
2. `image_gen` 返回图片后，必须检查实际像素尺寸和宽高比，不能相信提示词或文件名。
3. 最终文件必须精确为 `1080 × 1440`；不得交付 `2:3`、`16:9`、正方形或多页拼接图作为单页轮播。
4. 在 macOS 上优先运行 `scripts/normalize_3x4.sh input.png output.png`。该脚本会对白底图片补白或裁切，再导出 `1080 × 1440`；其他环境执行等价的像素归一化。
5. 归一化后再次检查尺寸；检查失败时重新处理，不能把原始比例图片交付给用户。

## 核心流程

1. 获取论文内容：PDF、链接、摘要、用户笔记或正文。
2. 提取论文主线，不按章节机械复述。
3. 按 7 步 schema 输出：一句话总结、解决的问题、核心方法、关键结果、最大创新、主要局限、启发。
4. 判断适合的发布形态：
   - `1-3 页`：快速分享、读后感、论文地图。
   - `6-8 页`：完整小红书论文解读。
5. 先生成 Paper Map，再生成单页生图提示词。
6. 中文标题、关键术语、长句和引用优先后期排版；不要依赖生图模型生成长中文。
7. 核查论文事实、贡献边界、结果描述和局限，不把作者没有证明的内容说成结论。

## 必须读取的参考

- 7 步总结结构：`references/paper-summary-schema.md`
- Research Notebook 视觉规则：`references/research-notebook-style.md`
- 小红书论文轮播模板：`references/xiaohongshu-paper-carousel.md`
- Loop Engineering 示例：`references/loop-engineering-example.md`
- QA 清单：`references/qa-checklist.md`

## 生图策略

优先生成“漂亮但少字”的 Research Notebook / Excalidraw 风格图：

- 英文短标签可以直接放进生图，例如 `Paper Map`、`Problem`、`Method`、`Risks`。
- 中文长标题、中文总结、公式、数据、引用、作者名和论文题目，优先作为后期 overlay 文案。
- 若用户明确要求中文在图内，控制在极短短语，并在生成后检查错字。

## 发布文案

先读取 `references/xiaohongshu-copywriting.md`。发布文案必须是可直接粘贴到小红书的格式，不得只给论文摘要式的一段说明。

交付图片后，必须给出与该轮播一一对应、可直接发布的以下内容：

```text
标题：1 个最终标题，另附 2 个备选标题
正文/简介：4-7 个短段，使用 4-8 个有语义的 emoji，至少 4 个分点；说明论文问题、关键 insight 和读者值得保存的原因
标签：5-10 个精准标签，覆盖论文主题、领域和阅读场景
```

标题优先呈现论文的核心冲突或反直觉结论；正文要有 `📌`、`✅`、`📈`、`⚠️`、`💡`、`💾` 等清晰层次，并严格区分作者结果与个人启发；标签不得使用无关热门词。

## 禁止

- 把论文目录改写成小红书内容。
- 只输出文字总结，不给视觉结构。
- 让生图模型直接生成大段中文。
- 夸大论文贡献或省略主要局限。
- 把论文正式 Figure 和论文阅读分享图混为一谈。
- 未经用户要求使用 16:9。
