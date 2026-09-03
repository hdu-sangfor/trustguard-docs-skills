# TrustGuard Docs Skills

面向 Codex、ChatGPT 和兼容 skill 规范的宿主环境的 TrustGuard 文档技能集合。
这些 skill 用于竞赛材料写作、技术架构图重绘和文档交付规范化，适合中国国际大学生创新大赛、挑战杯等项目材料。

## Included skills

| Skill | 用途 | 入口 |
| --- | --- | --- |
| `competition-doc-humanizer` | 撰写、改写和审阅中文竞赛材料，保持事实和技术术语准确，并检查 Word 版式 | [`trustguard-docs-write-skill`](trustguard-docs-write-skill/) |
| `trustguard-architecture-diagram` | 将架构图、流程图和 RAG/MCP/Agent 工作流重绘为深色 TrustGuard 技术图表风格 | [`trustguard-dark-architecture-diagram-skill`](trustguard-dark-architecture-diagram-skill/) |
| `trustguard-light-architecture-diagram` | 将技术图表重绘为白底、薄荷绿/青色的亮色竞赛文档风格 | [`trustguard-light-architecture-diagram-skill`](trustguard-light-architecture-diagram-skill/) |

每个目录都包含必需的 `SKILL.md`，以及可选的 `references/`、`assets/` 和 `agents/openai.yaml`。请按需单独安装某个 skill，或将整个仓库放入 skill 搜索路径。

## Installation

将需要的 skill 目录复制到 Codex skills 目录：

```powershell
$skillsDir = Join-Path $env:USERPROFILE ".codex\skills"
Copy-Item .\trustguard-docs-write-skill $skillsDir\competition-doc-humanizer -Recurse
Copy-Item .\trustguard-dark-architecture-diagram-skill $skillsDir\trustguard-architecture-diagram -Recurse
Copy-Item .\trustguard-light-architecture-diagram-skill $skillsDir\trustguard-light-architecture-diagram -Recurse
```

也可以在支持显式调用的环境中使用：

```text
$competition-doc-humanizer
$trustguard-architecture-diagram
$trustguard-light-architecture-diagram
```

具体提示词、参考资料和视觉资产请查看对应目录的 README 与 `SKILL.md`。

## Validation

修改 skill 后，使用 Codex skill-creator 提供的校验器检查 frontmatter、命名和脚手架占位符：

```powershell
$env:PYTHONUTF8 = "1"
$validator = Join-Path $env:USERPROFILE ".codex\skills\.system\skill-creator\scripts\quick_validate.py"
Get-ChildItem -Directory | ForEach-Object { python $validator $_.FullName }
```

校验器不能替代对生成图、文档版式和引用来源的人工检查。

## Third-party material

`competition-doc-humanizer` 的来源与适配说明见其 [`THIRD_PARTY_NOTICES.md`](trustguard-docs-write-skill/THIRD_PARTY_NOTICES.md)。使用或再发布前请同时遵守其中列出的第三方许可证和来源要求。

## Contributing

欢迎提交问题、改进建议和 pull request。请先阅读 [`CONTRIBUTING.md`](CONTRIBUTING.md)，并确保所有受影响的 skill 通过校验。

## License

除第三方材料另有说明外，本仓库内容以 [MIT License](LICENSE) 发布。
