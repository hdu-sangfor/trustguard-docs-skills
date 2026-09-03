# Transformation Guide

## 1. Extract the source before styling

Create an internal content map in this order:

1. **Canvas orientation**: landscape or tall workflow.
2. **Sections**: group labels and dashed subsystem boundaries.
3. **Nodes**: exact text, node role, hierarchy level.
4. **Edges**: source → target, arrow direction, connector label.
5. **Special semantics**: decision, pause, manual review, success output, retry/failure.
6. **Topology**: fan-out, fan-in, loop, optional branch, terminal state.

Do not begin visual restyling until this map is complete.

## 2. Assign style roles

Map source elements to TrustGuard roles:

- Ordinary process/service/data node → cyan card.
- Phase/stage title → cyan card with cyan title text.
- Decision condition → purple diamond.
- Pause/manual review/forced branch → purple rectangular card.
- Important clean/ready output → green card, only if truly semantically special.
- Error/retry/compensation → orange dashed path.
- Logical subsystem → blue dashed boundary.

If the source has color that is merely decorative, discard it and use these semantic roles instead.

## 3. Re-layout without changing topology

A style conversion may improve alignment and spacing while preserving logic.

Allowed layout improvements:

- Align cards to a grid.
- Equalize sibling widths.
- Move labels to prevent collisions.
- Replace curved connectors with orthogonal elbows.
- Increase canvas dimensions to improve readability.
- Recenter fan-out/fan-in groups.

Not allowed unless explicitly requested:

- Combining nodes.
- Deleting repeated nodes.
- Reordering phases.
- Reversing arrows.
- Changing branch meaning.
- Renaming technical components.

## 4. Prompt recipe for image-editing systems

When a raster style-transfer tool is appropriate, use instructions equivalent to:

> Use the uploaded diagram as the authoritative source for content, topology, labels, node count, and arrow direction. Preserve every technical label exactly. Restyle only the visual presentation into a clean TrustGuard cybersecurity architecture-diagram language: deep navy `#031226` background, dark blue `#082743` cards, crisp cyan `#55D9FC` outlines and orthogonal arrow connectors, white semibold body text, cyan phase titles, purple decision/control branches, optional restrained green only for explicit successful outputs. Use slight corner rounding, consistent grid alignment, generous spacing, no decorative icons, no 3D, no glassmorphism, no heavy glow, no sci-fi particles. The result must look like a formal Challenge Cup technical document figure, not an AI poster. Do not add, remove, paraphrase, translate, or hallucinate any node or text.

If the system cannot guarantee label fidelity, switch to vector reconstruction.

## 5. Vector reconstruction recipe

For SVG or programmatic drawing:

1. Set the canvas and background.
2. Define reusable classes for standard card, purple control card, success card, phase text, body text, muted annotation, connectors, and dashed boundary.
3. Draw connectors behind cards where possible.
4. Draw cards and decision shapes.
5. Add text last to guarantee readability.
6. Keep text centered vertically and horizontally unless a card intentionally contains title + subtitle.
7. Add arrow markers as filled triangles matching the connector color.
8. Render a PNG preview and inspect at 100% and page-width scale.

## 6. Batch normalization

For a multi-figure document, maintain a shared normalization sheet:

- Canvas class.
- Main background.
- Standard card fill/stroke.
- Primary line width.
- Standard body font size.
- Phase font size.
- Corner radius.
- Semantic accent mapping.

Do not “improve” one diagram with a different visual language mid-document.

## 7. Final QA

Check these failure modes explicitly:

- Chinese characters changed or garbled.
- `ATT&CK`, API names, paths, or file names altered.
- Arrowheads missing after rasterization.
- Branch labels detached from their branches.
- Cyan border too dim against the navy background.
- Green used as decorative accent rather than semantic success.
- Purple used for ordinary nodes, weakening its control-flow meaning.
- Cards have inconsistent corner radii or stroke widths.
- Diagram contains unnecessary icons, shields, robots, hexagons, or circuit wallpaper.
- Dense areas have tiny fonts while empty areas remain unused.

The output is ready only when both **technical fidelity** and **visual consistency** pass.
