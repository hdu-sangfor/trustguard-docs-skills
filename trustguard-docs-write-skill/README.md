# Competition Document Humanizer

用于中国国际大学生创新大赛（原“互联网+”）、挑战杯等竞赛材料的中文写作、改写、审校和 Word 版式规范化。

## 能力

- 保留项目事实、数字、技术术语、引用和边界，减少空泛或模板化表达。
- 支持申报书、商业计划书、设计/开发/测试文档、总结报告、答辩稿、PPT 文案和演示视频脚本。
- 按需检查摘要编号、标题层级、图表题注、页眉页脚、页码体系、表格分页和正文对齐。
- 提供竞赛写作框架、术语约定、去 AI 味规则和可复用示例。

## 安装与使用

将本目录复制到 Codex 的 skills 目录，并以 `competition-doc-humanizer` 作为 skill 名称：

```powershell
$skillsDir = Join-Path $env:USERPROFILE ".codex\skills"
Copy-Item .\trustguard-docs-write-skill $skillsDir\competition-doc-humanizer -Recurse
```

在支持显式调用的环境中，可使用 `$competition-doc-humanizer`，例如：

> 使用 `$competition-doc-humanizer`，保留所有技术术语和实测数据，把这段项目介绍改写成挑战杯申报书风格，并检查标题和图表题注格式。

入口规则见 [`SKILL.md`](SKILL.md)。详细资料位于 [`references/`](references/)，第三方来源和许可证说明见 [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md)。

## 注意事项

该 skill 不会替用户补造市场规模、测试结果、专利奖项、客户或部署情况。资料不足时，请补充可核验数据或使用明确占位符。
