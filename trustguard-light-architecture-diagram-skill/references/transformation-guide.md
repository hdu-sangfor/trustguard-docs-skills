# Transformation Guide

## 1. Extract the source before styling

Create an internal content map in this order:

1. **Canvas orientation**: landscape, tall workflow, or near-square research framework.
2. **Sections**: group labels, stage boundaries, side columns, resource layers, and major bands.
3. **Nodes**: exact text, node role, hierarchy level, icon if semantically necessary.
4. **Edges**: source → target, arrow direction, connector label, shared rail/junction.
5. **Special semantics**: protocol, decision, pause/manual review, validated output, warning/retry/failure.
6. **Topology**: fan-out, fan-in, loop, optional branch, terminal state.

Do not begin visual restyling until this map is complete.

## 2. Choose the closest bright layout family

Use `references/example-index.md` and the bundled assets.

- Execution/service chain with phases → **stage architecture**.
- Platform in the center with data/users/resources around it → **research framework**.
- Strong sequential integrated process → **pipeline spine**.
- Capability evolution or multi-level technical route → **layered roadmap**.

The reference image controls visual grammar and composition only. Never copy its labels/content into the user's diagram.

## 3. Assign style roles

Map source elements to bright TrustGuard roles:

- Ordinary process/service/data node → mint/white light card.
- Phase/platform title → mint header band or dark-navy title over a light panel.
- Normal data/control flow → blue connector.
- Protocol/control/decision → lavender card/connector.
- Important ready/validated output → light green card, only if semantically special.
- Error/retry/compensation → orange dashed path.
- Logical subsystem/stage → light-blue dashed rounded boundary.
- Major integrated production line → saturated blue or restrained blue→teal arrow spine.

Discard decorative colors from the source unless they carry real semantics.

## 4. Re-layout without changing topology

Allowed improvements:

- Align cards to a grid.
- Equalize sibling widths.
- Recenter branches and shared rails.
- Move labels to prevent collisions.
- Replace tangled curves with orthogonal elbows in stage architecture.
- Use a stronger central spine in pipeline figures.
- Increase canvas dimensions to improve readability.
- Rebalance left/right side columns in research-framework figures.

Not allowed unless explicitly requested:

- Combining nodes.
- Deleting repeated nodes.
- Reordering phases.
- Reversing arrows.
- Changing branch meaning.
- Renaming technical components.
- Translating technical English labels.

## 5. Raster style-transfer recipe

When a raster image-editing system is appropriate, use instructions equivalent to:

> Use the uploaded source diagram as the authoritative specification for content, topology, labels, node count, group boundaries, and arrow direction. Preserve every technical label exactly. Restyle only the presentation into the bright TrustGuard competition-document language: white or very light cool-gray background; soft mint/teal platform blocks; white/light cards with thin teal or sky-blue borders; crisp dark navy text; blue data-flow arrows; lavender protocol/control cards and connectors; light-blue dashed stage boundaries; optional restrained light-green success state; one blue→teal gradient only for a major pipeline spine when the composition needs it. Use clean sans-serif Chinese typography, rounded rectangles, balanced grid alignment, generous whitespace, and minimal flat icons. No dark navy canvas, neon glow, black dashboard panels, sci-fi particles, glassmorphism, 3D, heavy shadow, decorative AI imagery, or invented nodes. Do not add, remove, paraphrase, translate, or hallucinate any text or relationship.

Reject the raster result if Chinese text is garbled, technical names change, nodes disappear, or topology drifts. Switch to vector reconstruction instead.

## 6. Vector reconstruction recipe

For SVG/programmatic drawing:

1. Set a white or `#F7FAFC` canvas.
2. Define shared classes for stage boundary, light mint card, light blue card, lavender protocol/control card, success card, primary/secondary text, blue connector, purple connector, orange retry connector, and header band.
3. Lay out group panels/boundaries first.
4. Draw connectors behind cards where possible; use shared rails for fan-out/fan-in.
5. Draw cards, bands, and semantic icons.
6. Add text last to guarantee legibility.
7. Keep title + subtitle alignment consistent across same-level cards.
8. Use compact filled arrow markers matching connector color.
9. Render a PNG preview and inspect at 100% and at document page width.
10. If the user requested PNG only, still keep the SVG as the source of truth when text density is high.

Use `assets/style-reference-vector.svg` as a token/layout example, not as a content template.

## 7. Batch normalization

For a multi-figure document, maintain a shared normalization sheet:

- Canvas class.
- Canvas color.
- Primary mint fill.
- Standard card fill/stroke.
- Primary blue connector width.
- Lavender semantic mapping.
- Standard body font size.
- Stage/header font size.
- Corner radius.
- Boundary dash pattern.
- Optional shadow intensity.

Do not make one diagram noticeably more saturated, more rounded, darker, or more decorative than the others.

## 8. Final QA

Check these failure modes explicitly:

- Chinese characters changed or garbled.
- `ATT&CK`, API names, paths, file names, or case-sensitive tokens altered.
- Arrowheads missing after rasterization.
- Branch labels detached from their branches.
- White cards disappear against the canvas because borders are too faint.
- Mint/teal fills become so saturated that the diagram looks like a marketing poster.
- Lavender is used for ordinary nodes, weakening protocol/control meaning.
- Green/orange appears decoratively without source semantics.
- Boundaries, cards, or labels use inconsistent corner radii or stroke widths.
- Shadows are heavy enough to resemble web UI cards.
- Dense areas use tiny fonts while large empty areas remain unused.
- The final result accidentally reverts to a dark/navy background.

The output is ready only when both **technical fidelity** and **bright visual consistency** pass.
