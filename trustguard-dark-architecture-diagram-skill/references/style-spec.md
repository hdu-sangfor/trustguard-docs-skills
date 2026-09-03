# TrustGuard Architecture Diagram Style Specification

## 1. Visual identity

The visual signature is a **deep navy technical canvas + cyan line architecture + restrained semantic accents**. It should feel like a polished cybersecurity/AI engineering document figure, not a promotional poster.

## 2. Core palette

Use these values as defaults; small anti-aliasing variations are fine.

| Role | Color | Usage |
|---|---|---|
| Canvas | `#031226` | Primary full-canvas background |
| Canvas alternate | `#031023` → `#0A203D` | Optional very subtle two-stop background gradient |
| Card fill | `#082743` | Default node/card interior |
| Secondary card fill | `#0D355B` | Nested/secondary surface when hierarchy needs separation |
| Main cyan | `#55D9FC` | Connectors, arrowheads, node outlines |
| Cyan accent | `#31D7F8` | Phase titles / emphasized labels |
| Soft cyan | `#96CBED` | Secondary annotations or subtitles |
| Primary text | `#EFF4F8` | Ordinary node text |
| Muted text | `#A9BFD4` | Small notes / branch labels |
| Purple | `#9658E9` | Decision/control/optional-review outline and connectors |
| Purple fill | `#1B183E` | Decision/control cards |
| Group boundary blue | `#556DE1` | Dashed logical-region border |
| Success green fill | `#5C8E3D` | Important validated output only |
| Success green line | `#91D566` | Success border/text accent |
| Failure orange | `#FFAD4D` | Failure/retry/compensation path only |

Do not use all accent colors in every figure. The default should be navy + cyan + white.

## 3. Canvas and composition

### Landscape architecture

- Default: `1600×900`; use `1920×1080` for final PPT/document export.
- Content occupancy: roughly 78–90% of usable width and 72–86% of usable height.
- Outer margin: about 3–5% of canvas width.

### Tall workflow

- Default class: roughly `1200×1500` or equivalent aspect ratio.
- Use when the process has many sequential phases.
- Keep a central vertical spine with balanced side branches.

Never squeeze a dense diagram into 16:9 by making text tiny. Increase the canvas or use tall orientation.

## 4. Node geometry

### Standard card

- Fill: `#082743`
- Stroke: `#55D9FC`
- Stroke width at 1600 px canvas: `2.5–3.5 px`
- Corner radius: `6–12 px`; slightly rounded rectangle, not pill-shaped
- Internal horizontal padding: `18–28 px`
- Internal vertical padding: `14–22 px`
- Typical node height: `64–92 px`

### Phase/header card

- Same geometry as standard card.
- Text uses cyan accent and stronger weight.
- May be 1.1–1.3× wider than ordinary sibling nodes.

### Decision diamond

- Fill: `#1B183E`
- Stroke: `#9658E9`
- Stroke width: `3–4 px`
- Text: purple or white depending on contrast
- Use only for actual decisions/branching conditions.

### Control/optional card

- Rectangular card using purple fill/stroke.
- Suitable for pause, manual review, forced recrawl, optional approval, retry-control, etc.

### Success/output highlight

- Fill: `#5C8E3D`
- Stroke: `#91D566`
- Use only for key clean output, ready state, final validated artifact, or another explicitly successful semantic milestone.

### Group boundary

- No fill.
- Stroke: `#556DE1`
- Width: `3.5–4.5 px`
- Dash pattern near `18 10` at 1600 px canvas.
- Keep at least `22–32 px` clearance from enclosed cards.

## 5. Connectors

- Primary stroke: `#55D9FC`
- Primary width: `3–4 px` at 1600 px canvas.
- Major spine or critical pipeline: up to `4–5 px`.
- Arrowhead: compact filled triangle, same color as line.
- Routing: orthogonal elbows, usually one or two bends.
- Junctions: align to shared horizontal/vertical rails rather than drawing many independent lines.
- Minimum visual clearance between a connector and unrelated text/card: about `12–18 px`.

Semantic connector colors:

- Purple for control/decision branches.
- Orange dashed for failure/retry/compensation.
- Cyan for normal data/control flow.

Avoid curved Bezier connectors unless the original topology truly requires them.

## 6. Typography

Recommended fallback stack:

`Microsoft YaHei, Noto Sans CJK SC, Source Han Sans SC, Arial, sans-serif`

At a `1600×900` canvas:

- Figure title if present: `34–42 px`, weight `800`.
- Major section/group title: `22–28 px`, weight `750–800`.
- Phase card title: `20–24 px`, weight `700–800`, usually cyan.
- Standard node text: `17–21 px`, weight `600–700`, white.
- Small branch/annotation text: `14–16 px`, weight `500–600`, muted white/blue.

Scale all text proportionally with canvas dimensions. Do not reduce standard node text below a visually equivalent 16 px merely to fit more content.

## 7. Hierarchy and spacing

- Sibling cards: align edges and keep uniform widths where practical.
- Horizontal sibling gap: roughly `24–44 px`.
- Vertical stage gap: roughly `24–46 px`.
- Larger separation between major phases: `42–72 px`.
- Keep branch labels close to the relevant connector, not floating in empty space.
- Use whitespace to express stage hierarchy instead of decorative separators.

## 8. Visual effects

Preferred:

- Flat fills.
- Crisp strokes.
- High contrast.
- Optional very restrained cyan halo on one critical hub only.
- Optional subtle navy background gradient.

Avoid:

- Heavy drop shadows.
- Bloom around every line.
- Texture noise.
- Grid backgrounds unless the user explicitly requests them.
- Decorative circuit patterns.
- 3D/extrusion.

## 9. Document-specific guidance

For competition documents and judges' review:

- Optimize for print/PDF clarity, not cinematic effect.
- Keep semantic color count low.
- Ensure all labels remain legible when the figure is scaled to page width.
- Prefer vector SVG for text-heavy diagrams.
- Preserve enough contrast for screenshots embedded in DOCX/PDF.
