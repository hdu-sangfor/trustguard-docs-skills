---
name: trustguard-light-architecture-diagram
description: Redraw technical architecture diagrams, flowcharts, research frameworks, data pipelines, RAG/MCP/Agent workflows, and system execution chains into the bright TrustGuard competition-document visual language while preserving labels and topology. Use when the user asks for a light/bright/white-background version, academic research-diagram styling, mint/teal/blue architecture figures, editable SVG/PNG output, or visual consistency with the bundled bright reference diagrams for Challenge Cup documents and PPTs.
---

# TrustGuard Light Architecture Diagram

Create competition-document architecture diagrams that look like one coherent **bright academic visual system** rather than unrelated flowcharts or dark dashboard graphics.

Read `references/style-spec.md` for exact visual tokens, `references/transformation-guide.md` for the redraw workflow, and `references/example-index.md` to choose the closest bundled visual anchor. Use the images in `assets/` as style/layout references when the host environment can access them.

## Core rule: content fidelity before styling

Treat the source diagram as a technical specification.

Before redrawing, extract and lock:

1. Every node and its exact text.
2. Every edge, arrow direction, merge, branch, and loop.
3. Decision/branch labels and success/failure/retry semantics.
4. Phase/group boundaries and section titles.
5. Technical names, capitalization, punctuation, file paths, API names, acronyms, and units.

Do not invent, delete, translate, normalize, or silently correct technical content unless the user explicitly requests content optimization. If text is unreadable, mark it unresolved instead of guessing.

## Choose the redraw mode

Follow the host environment's image/tool policy.

### Raster style-transfer mode

Use for a direct “按这个亮色风格重绘” request when the source image is present and label fidelity is simple enough to maintain.

- Use the source image as the authoritative content/topology reference.
- Apply only the bright TrustGuard visual system.
- Keep all labels, node count, group boundaries, and edge directions unchanged.
- Reject an output if Chinese/technical text is corrupted, nodes disappear, or topology changes.

### Vector reconstruction mode

Prefer SVG reconstruction when any of the following is true:

- The diagram will be inserted into a formal competition document or PPT.
- Exact Chinese/English typography matters.
- The user wants editable output.
- The source contains many technical labels, paths, APIs, acronyms, or dense branches.
- Generative editing would likely garble text.

Rebuild with the tokens in `references/style-spec.md`. If PNG is requested, render the validated SVG to PNG after the vector version is correct.

## Layout families

Choose one dominant family before drawing. Preserve source topology while improving spacing and alignment.

- **Stage architecture**: left-to-right subsystem/stage columns with dashed rounded boundaries. Best for execution chains, orchestration, service interactions, or Agent/Skill workflows.
- **Research framework**: central platform/capability blocks with side data/user columns and lower resource layer. Best for platform research framework figures.
- **Pipeline spine**: one strong horizontal arrow/spine with repeated capability stages above/below it. Best for production-line, integrated workflow, or lifecycle figures.
- **Layered roadmap**: vertically stacked discs/bands or level-by-level hierarchy with restrained translucent blue-violet layers. Best for research route or multi-level capability evolution.

For ordinary system architecture, default to **stage architecture**. For more than five sequential major phases, consider a tall top-to-bottom flow instead of shrinking text.

## Semantic color rules

Use color to encode meaning, not decoration.

- **Mint/teal**: default platform blocks, capability groups, ordinary architecture nodes, phase headers.
- **Blue**: normal data flow, primary connectors, major pipeline spine, technical structure.
- **Lavender/purple**: protocol channels, decisions, control flow, optional/manual-review branches.
- **Green**: validated/ready/success outputs only; use sparingly.
- **Orange**: warning, retry, compensation, degraded/failure paths only when present in the source.
- **Light blue dashed boundary**: logical subsystem, stage scope, or grouped processing region.

Keep the base canvas white or very light gray. Do not revert to the dark navy TrustGuard style unless the user explicitly asks for the dark version.

## Typography rules

- Use `Microsoft YaHei`, `Noto Sans CJK SC`, `Source Han Sans SC`, or another clean sans-serif Chinese font.
- Use dark navy/charcoal text on light surfaces; do not use white body text unless a saturated blue/teal band requires it.
- Use semibold/bold for section titles and primary node labels.
- Break long labels into balanced 2–3 lines rather than shrinking them excessively.
- Keep technical English names and acronyms intact, e.g. `MITRE ATT&CK`, `NVD`, `Qdrant`, `OpenSearch`, `Embedding`, `MCP`, `SkillResult`.
- Use monospace only for literal paths, URIs, commands, or code-like tokens when it improves clarity.

## Visual restraint

Target a clean research-project / competition-document infographic aesthetic.

Use:

- White or very light cool-gray canvas.
- Soft mint/teal/sky-blue fills with dark text.
- Rounded cards, thin crisp borders, and at most a faint low-opacity shadow.
- Orthogonal or simple straight connectors with compact arrowheads.
- Wide whitespace and symmetric alignment.
- One restrained blue→teal gradient only for a major spine/production-line arrow when the layout family calls for it.

Avoid:

- Dark navy full-canvas backgrounds, neon glow, sci-fi particles, circuit wallpaper, glassmorphism, metallic bevels, 3D cards, heavy gradients, or large shadows.
- Decorative AI/security icons that do not encode meaning.
- Multiple unrelated card styles.
- Curved spaghetti connectors or connectors crossing text.
- Excessive pills or oversized rounded corners.
- Pure black blocks that make the figure look like a dashboard rather than a formal research diagram.

Do not add a decorative figure title inside the graphic unless the source has one or the user requests it; competition documents usually provide figure captions separately.

## Batch consistency protocol

When processing multiple diagrams for the same document:

1. Reuse one canvas family and the exact tokens from `references/style-spec.md`.
2. Keep the same mint/blue/purple semantic mapping across all figures.
3. Reuse corner radii, stroke widths, arrowheads, header treatment, and text scale.
4. Keep phase labels and card hierarchy visually consistent.
5. Scale font/line weight by canvas size, not by individual diagram density.
6. Increase canvas dimensions instead of shrinking labels below readable size.

## Quality gate

Before delivering, verify all of the following:

- Node inventory matches the source.
- Edge directions, branch labels, merges, and loops match the source.
- No connector crosses text or passes through unrelated cards.
- No cropped cards, arrowheads, labels, or group boundaries.
- Text remains readable at normal document zoom and crisp after export.
- Canvas is white/light gray; mint/teal/blue is the dominant structural language.
- Purple/green/orange remain semantic accents, not decoration.
- Card fills stay visibly separated from the canvas without becoming dark UI panels.
- The result looks flat, balanced, grid-aligned, academic, and technical.
- No generative artifacts, misspellings, duplicated nodes, invented icons, or accidental content edits remain.

If technical text or topology is wrong, fix that before visual polish.

## Reference files

- `references/style-spec.md` — palette, dimensions, strokes, typography, card recipes, and layout tokens.
- `references/transformation-guide.md` — extraction, layout selection, raster/vector redraw recipes, and QA.
- `references/example-index.md` — how to use each bundled bright reference image without copying its content.
- `assets/style-reference-execution-chain.png` — primary stage-architecture reference; bright redraw of a technical execution chain.
- `assets/style-reference-framework.png` — research-framework composition with mint platform areas and side columns.
- `assets/style-reference-roadmap.png` — layered research-route composition with light blue/violet translucent structure.
- `assets/style-reference-pipeline.png` — large horizontal pipeline/production-line composition with blue→teal progression.
- `assets/style-reference-vector.svg` — editable vector anchor implementing the same bright visual language.
