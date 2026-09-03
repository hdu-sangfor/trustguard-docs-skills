# Bright Reference Index

Use these assets as **visual/layout anchors only**. Never copy their technical content into a user's diagram. Pick the closest reference family, then preserve the user's own labels and topology.

## 1. `assets/style-reference-execution-chain.png`

**Primary reference for stage-based architecture.**

Use when the source contains several left-to-right phases such as task preparation, scheduling, execution, and result return.

Key traits to reuse:

- White background.
- Four or more aligned dashed rounded stage boundaries.
- Dark-navy stage titles above each boundary.
- White/light mint cards with teal/sky-blue outlines.
- Blue normal-flow arrows and lavender protocol/control channels.
- Minimal line icons.
- Consistent card widths and baseline alignment.
- Compact legend below the diagram when the source needs one.

Example request pattern:

> 把这张暗色执行链改成亮色竞赛文档风格，保留所有节点、英文技术名和箭头关系，按阶段分栏，输出 SVG 和 PNG。

## 2. `assets/style-reference-framework.png`

**Reference for academic research-framework composition.**

Use when the source has a central platform or capability area, data/resource columns on one side, users/roles on the other, and infrastructure/resources at the bottom.

Key traits to reuse:

- Mint platform header bands.
- Soft gray-blue group panels.
- White nested cards.
- Side columns with repeated aligned items.
- Symmetric platform/capability blocks.
- Generous white margins and low visual noise.

Example request pattern:

> 参考亮色科研框架图，把我们的平台架构整理成“数据来源—核心平台—用户对象—底层资源”的结构，原有模块一个都不要丢。

## 3. `assets/style-reference-roadmap.png`

**Reference for layered research-route / capability-evolution composition.**

Use when the source is a high-level technical route, multi-level capability system, or roadmap with broad conceptual layers rather than many fine-grained service calls.

Key traits to reuse:

- White background with translucent blue/violet layered discs or bands.
- Strong center axis and clear vertical hierarchy.
- Dark text with blue/purple emphasis.
- Sparse callouts around the core rather than dense boxed UI.
- Controlled transparency; maintain print clarity.

Example request pattern:

> 把现有研究技术路线图改成白底蓝紫分层结构，保留原来的层级和关键技术，只优化空间层次和可读性。

## 4. `assets/style-reference-pipeline.png`

**Reference for integrated pipeline / production-line composition.**

Use when the source is strongly sequential and benefits from one dominant horizontal spine.

Key traits to reuse:

- Large blue structural arrow or blue→teal major spine.
- Repeated stage labels placed on/around the spine.
- Supporting capability lists above and below each stage.
- Strong left-to-right momentum.
- Minimal decorative elements; the spine carries the visual hierarchy.

Example request pattern:

> 把这张多阶段流程图改成一条横向一体化生产线，保留阶段顺序和上下支撑能力，整体使用白底蓝青配色。

## Reference selection rule

If more than one reference seems relevant, use this priority:

1. Preserve the user's topology.
2. Choose the layout family that minimizes line crossings and tiny text.
3. Prefer `style-reference-execution-chain.png` for ordinary technical architecture.
4. Borrow secondary traits from another reference only when they do not create a mixed visual language.
