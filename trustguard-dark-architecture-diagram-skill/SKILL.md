---
name: trustguard-architecture-diagram
description: "Restyle or redraw system architecture diagrams, process diagrams, data-flow diagrams, RAG/MCP/Agent/security workflows into the TrustGuard Challenge Cup visual language: deep navy canvas, dark blue cards, cyan outlines and orthogonal connectors, restrained white/cyan typography, purple control/decision branches, and optional green success highlights. Use when the user asks to make an existing diagram/image match the TrustGuard style, unify multiple diagrams for competition documents or PPTs, convert rough/white-background charts into this dark cyber style, or create a new technical diagram consistent with the bundled references. Preserve technical content and topology unless the user explicitly asks to optimize them."
---

# TrustGuard Architecture Diagram

Create competition-document architecture diagrams that look like one coherent visual system rather than unrelated flowcharts.

Read `references/style-spec.md` for exact visual tokens and `references/transformation-guide.md` for the redraw workflow. Use the bundled images in `assets/` as visual anchors when the environment can access them.

## Core rule: content fidelity before styling

Treat the source diagram as a technical specification, not merely a visual reference.

Before redrawing, extract and lock:

1. Every node and its exact text.
2. Every edge, arrow direction, merge, branch, and loop.
3. Decision labels such as “是/否”, “继续/暂停”, success/failure, or retry paths.
4. Phase/group boundaries and section titles.
5. Technical names, capitalization, punctuation, file paths, API names, acronyms, and units.

Do not invent, delete, translate, normalize, or silently correct technical content unless the user asks for content optimization. If text is unreadable, mark it as unresolved rather than guessing.

## Choose the redraw mode

Follow the host environment's image/tool policy.

### Raster style-transfer mode

Use for a straightforward “把这张图改成这种风格” request when the source image is present and text fidelity can be maintained.

- Use the source image as the content/topology reference.
- Apply the TrustGuard visual system only.
- Keep all labels, node count, and edge directions unchanged.
- Reject an output if generative editing corrupts Chinese/technical text, loses nodes, or changes topology.

### Vector reconstruction mode

Prefer SVG reconstruction when any of the following is true:

- The diagram will be inserted into a formal competition document or PPT.
- Exact Chinese/English typography matters.
- The user wants editable output.
- The source contains many technical labels, paths, APIs, or acronyms.
- A generative image edit would likely garble text.

Rebuild the diagram with the style tokens in `references/style-spec.md`. If the user wants PNG, render the SVG to PNG after the vector version is correct.

## Layout logic

Choose one dominant flow direction per figure.

- Use **left-to-right** for system pipelines, service interactions, crawler/data-processing flows, or wide architecture views.
- Use **top-to-bottom** for long ingestion pipelines, phased workflows, ETL/RAG processes, or diagrams with more than five major stages.
- Place major phases on a clear central spine.
- Align fan-out siblings to a shared grid and merge them symmetrically.
- Route connectors orthogonally with horizontal/vertical elbows. Avoid arbitrary diagonals and avoid line crossings.
- Use consistent card widths within the same hierarchy level.
- Keep outer margins generous enough that the diagram never touches the canvas edge.
- Do not add a decorative title inside the figure unless the source has one or the user asks for it; competition documents usually provide captions separately.

For batch work, keep the same palette, stroke widths, corner radii, typography, arrowheads, and semantic colors across all figures.

## Semantic color rules

Use color to encode meaning, not decoration.

- **Cyan**: default architecture nodes, data flow, ordinary processing, phase headers.
- **Purple**: decisions, control flow, optional/pause/manual-review branches, exceptional control states.
- **Green**: important successful intermediate outputs, validated artifacts, “ready” states. Use sparingly.
- **Orange**: failure, retry, compensation, degraded paths. Use only when the source actually contains that semantic.
- **Blue dashed boundary**: logical subsystem, stage scope, or grouped processing region.

Never introduce extra colors merely to make the diagram “more technological”.

## Typography rules

- Use `Microsoft YaHei`, `Noto Sans CJK SC`, or another clean sans-serif Chinese font.
- Use white for ordinary node text and bright cyan for phase/section emphasis.
- Use semibold/bold weights; keep text flat without glow, outline, bevel, or 3D effects.
- Break long labels into two or three balanced lines rather than shrinking them excessively.
- Keep English product names and acronyms intact, e.g. `MITRE ATT&CK`, `NVD`, `Qdrant`, `OpenSearch`, `Embedding`, `MCP`.
- Use monospace only when a literal path, URI, command, or code-like token benefits from it.

## Visual restraint

The target is a clean technical competition-document aesthetic, not a sci-fi poster.

Do not use:

- 3D cards, glassmorphism, metallic bevels, heavy gradients, or lens flare.
- Dense particles, circuit-board wallpaper, random security icons, or decorative AI imagery.
- Large outer glows or fuzzy neon that reduce print clarity.
- Multiple unrelated box styles.
- Curved “spaghetti” connectors.
- Excessive rounded pills.
- Shadows that make the diagram look like a dashboard UI rather than an architecture figure.

A very subtle background gradient or restrained cyan glow is acceptable only if it does not weaken the flat diagram language.

## Batch consistency protocol

When processing multiple diagrams for the same document:

1. Select one canvas family: landscape (`1600×900` or `1920×1080`) or tall-flow (`1200×1500`-class) based on topology.
2. Reuse the exact same style tokens from `references/style-spec.md`.
3. Keep the same semantic meaning for purple/green/orange throughout the document.
4. Keep phase labels and card hierarchy visually consistent.
5. Match line weight and text scale by canvas size, not by individual diagram density.
6. Prefer fewer, larger readable nodes over microscopic text; if the topology is too dense, increase canvas dimensions instead of shrinking fonts.

## Quality gate

Before delivering, verify all of the following:

- Node inventory matches the source.
- Edge directions and branch labels match the source.
- No connector crosses text or passes through unrelated cards.
- No cropped cards, arrowheads, labels, or group boundaries.
- Text is readable at normal document zoom and remains crisp when exported.
- Cyan is the dominant structural color; purple/green/orange remain semantic accents.
- Background is dark navy, not pure black.
- Card fill remains visibly lighter than the background.
- The result looks flat, disciplined, grid-aligned, and technical.
- No generative artifacts, misspellings, duplicated nodes, or invented icons are present.

If any text or topology is wrong, fix that before visual polish.

## Reference files

- `references/style-spec.md` — exact palette, dimensions, strokes, typography, and shape recipes.
- `references/transformation-guide.md` — extraction, layout, prompt recipe, and QA workflow.
- `assets/style-reference-wide.png` — wide crawler/process example.
- `assets/style-reference-portrait.png` — tall phase-pipeline example.
- `assets/style-reference-portrait-highlight.png` — tall example with restrained green output highlights.
- `assets/style-reference-vector.svg` — vector reference with the same visual language and additional semantic states.
