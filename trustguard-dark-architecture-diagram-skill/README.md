# TrustGuard Architecture Diagram

一个用于 Codex 的 skill，把系统架构图、流程图、数据流图以及 RAG/MCP/Agent/安全工作流统一重绘为 TrustGuard Challenge Cup 的技术图表风格。

## 能力

- 保留源图的节点、技术文本、箭头方向、分支语义和拓扑结构。
- 采用深海军蓝画布、深蓝卡片、青色正交连线和克制的语义色。
- 根据密度选择横向架构图或纵向流程图画布。
- 文本密集或需要可编辑输出时，优先重建 SVG，再按需导出 PNG。
- 支持单图重绘，也支持同一文档中的批量风格统一。

## 使用

将本目录放入 Codex 的 skills 目录，例如：

```text
%CODEX_HOME%\skills\trustguard-architecture-diagram\
```

也可以在支持显式 skill 调用的环境中使用 `$trustguard-architecture-diagram`。示例请求：

> 使用 `$trustguard-architecture-diagram`，把这张流程图重绘成 TrustGuard 风格，保留所有中文、API 名称和箭头关系，并输出可编辑 SVG。

这个 skill 提供风格规范和重绘决策，不包含独立的图像渲染器；实际输出格式取决于宿主环境可用的图像或 SVG 工具。

## 目录

```text
SKILL.md                         入口说明和工作流
references/style-spec.md         颜色、尺寸、线宽和字体规范
references/transformation-guide.md  内容提取、重排和质量检查
assets/                          风格参考图和图标
agents/openai.yaml               Codex UI 元数据
```

## 质量要求

提交或发布前，请确认节点清单、边方向和分支标签与源图一致；技术文本没有被改写或乱码；连线没有穿过卡片或文本；导出后在 100% 和文档页宽下都清晰可读。详细检查项见 `SKILL.md` 和 `references/transformation-guide.md`。

## 开发与校验

修改后运行 skill-creator 提供的校验器：

```powershell
$env:PYTHONUTF8 = "1"
python $env:USERPROFILE\.codex\skills\.system\skill-creator\scripts\quick_validate.py .
```

校验器检查 frontmatter、命名和未完成的脚手架占位符；它不会替代对生成图的人工视觉检查。

## 许可证

除第三方材料另有说明外，本 skill 遵循仓库根目录的 [MIT License](../LICENSE)。参考图和图标资产如有单独来源或限制，以相应说明为准。
