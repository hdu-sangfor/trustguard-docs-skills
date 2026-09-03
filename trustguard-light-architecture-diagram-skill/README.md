# TrustGuard Light Architecture Diagram

一个用于把系统架构图、流程图、研究框架图、RAG/MCP/Agent/Skill 工作流统一重绘为 **亮色 TrustGuard 竞赛文档风格** 的 Skill。

它与原来的 `trustguard-architecture-diagram` 分工明确：原 Skill 采用深海军蓝暗色技术风格，本 Skill 采用白底、薄荷绿/青色/蓝色为主的科研图表风格，更适合 Word 总结报告、技术文档和亮底 PPT 页面。

## 能力

- 保留源图节点、技术文本、箭头方向、分支语义和拓扑结构。
- 支持阶段分栏架构、科研框架、横向一体化管线、分层研究路线四类亮色布局。
- 采用白/浅灰画布、薄荷绿/青色结构块、蓝色数据流和克制的紫色协议/控制语义。
- 文本密集或需要可编辑输出时，优先重建 SVG，再按需导出 PNG。
- 支持单图重绘，也支持同一文档中的批量风格统一。

## 使用示例

> 使用 `$trustguard-light-architecture-diagram`，把这张暗色架构图重绘成白底亮色竞赛文档风格，保留所有中文、API 名称和箭头关系，并输出可编辑 SVG。

> 使用 `$trustguard-light-architecture-diagram`，参考内置的亮色阶段架构案例，把这张 Skill 执行链改成薄荷绿 + 蓝色 + 紫色协议通道的风格。

## 目录

```text
SKILL.md                              入口说明和工作流
references/style-spec.md              亮色颜色、尺寸、线宽和字体规范
references/transformation-guide.md    内容提取、布局选择、重绘和质量检查
references/example-index.md           四类内置参考案例的使用说明
assets/                               亮色参考图、SVG 参考和图标
agents/openai.yaml                    ChatGPT/Codex UI 元数据
```

## 质量要求

提交或发布前，确认节点清单、箭头方向、分支标签与源图一致；技术文本没有被改写或乱码；连线没有穿过卡片或文字；导出后在 100% 和文档页宽下都清晰可读；整体保持白底、薄荷绿/青蓝结构和深色文字，不回退为暗色仪表盘风格。

## 许可证

除第三方材料另有说明外，本 skill 遵循仓库根目录的 [MIT License](../LICENSE)。参考图和图标资产如有单独来源或限制，以相应说明为准。
