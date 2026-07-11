# 配图质量门槛

论文分享图要像清爽的研究笔记，而不是堆满空框的 PPT 线框图。结构丰富必须服务于论文主线。

## 构图硬规则

- 每页只保留一个主线动作或论文关系，配 2-3 个有内容的辅助模块。
- 页面最多 4 个边框模块；每个模块都必须有真实论文信息、箭头关系或结论，禁止空卡片、占位横线、虚假表格和无意义虚线框。
- 标题区独立占顶部 12%-16%，标题、副标题和页码不能压到 Paper Map 或主结构上。
- Paper Map 使用一条清楚的主脊柱：Problem → Method → Result → Insight；不要做成没有阅读顺序的模块墙。
- 留白只用于分隔内容，不得出现大块“准备放内容但没有内容”的空白。

## 生图提示词必须包含

```text
finished Xiaohongshu research notebook card, not a wireframe,
no empty boxes, no placeholder lines, no blank panels,
no overlapping title, no clipped labels, no fake metrics,
one clear paper storyline plus 2-3 compact annotations,
clear reading order, purposeful whitespace
```

论文题目、指标、公式和长中文优先用可控的后期排版；如果当前环境不能做后期排版，就减少图中文字并重新生成，不能交付有错字、重叠或占位线的图片。

## 生成后拒绝条件

出现以下任一情况，必须重新生成或重新排版：

- 标题压线、越界、重叠或被装饰遮挡。
- 出现空白卡片、灰色占位线、无意义的模块框。
- 论文事实、指标、方法名或结论乱码、重复或截断。
- 箭头没有清晰起点和终点，或者 Paper Map 无法一眼读出主线。
- 把论文正式 Figure 画成唯一内容，缺少问题、贡献或局限。
- 页面一眼看不出读者应该记住什么。
