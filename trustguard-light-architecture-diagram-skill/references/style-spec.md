# TrustGuard Light Architecture Diagram Style Specification

## 1. Visual identity

The visual signature is a **white/light academic canvas + mint/teal structural blocks + blue flow + restrained lavender semantic accents**. It should feel like a polished research-project architecture figure for a Challenge Cup document or PPT, not a dark cybersecurity dashboard.

## 2. Core palette

Use these values as defaults; small anti-aliasing variations are fine.

| Role | Color | Usage |
|---|---|---|
| Canvas | `#FFFFFF` | Primary full-canvas background |
| Canvas alternate | `#F7FAFC` | Optional very light cool-gray background |
| Group panel | `#EEF4F5` | Soft subsystem/platform backing surface |
| Primary mint | `#9EDBCB` | Major platform headers, capability bands, section emphasis |
| Mint light | `#EAF7F3` | Default mint card fill |
| Teal | `#35B8AA` | Mint-family outlines, icons, secondary connectors |
| Sky blue | `#70B7E8` | Secondary block accents, information areas |
| Main blue | `#3F86DF` | Primary data flow, arrowheads, major technical structure |
| Deep blue | `#1F62CA` | Major pipeline spine / strong structural accent |
| Lavender | `#8B66E8` | Protocol, decision, control, optional branches |
| Lavender fill | `#F3EEFF` | Protocol/control cards |
| Boundary blue | `#82AEEF` | Dashed logical-region/stage border |
| Primary text | `#12233D` | Titles and ordinary labels |
| Secondary text | `#566980` | Subtitles and annotations |
| Success fill | `#EAF7EE` | Validated/ready/success output only |
| Success line | `#70B588` | Success border/icon |
| Failure orange | `#EFA34A` | Failure/retry/compensation only |

Do not use every accent in every figure. Default to white + mint/teal + blue + dark text.

## 3. Canvas and composition

### Landscape architecture

- Default: `1600×900`; use `1920×1080` for final PPT/document export.
- Content occupancy: about 82–92% of usable width and 74–88% of usable height.
- Outer margin: about 3–5% of canvas width.
- Keep at least 24–36 px clear space between the outermost card and canvas edge at 1600 px width.

### Tall research/workflow figure

- Default class: `1200×1400` to `1400×1600` or equivalent aspect ratio.
- Use when a source has many sequential phases or a vertical research-route hierarchy.
- Keep a central spine and balance side callouts rather than making text microscopic.

Never force a dense diagram into 16:9 by shrinking labels. Increase canvas size or change orientation.

## 4. Node and panel geometry

### Standard light card

- Fill: `#FFFFFF` or `#EAF7F3` depending on hierarchy.
- Stroke: `#7BCFC2` for mint-family cards or `#8BB9EA` for blue-family cards.
- Stroke width at 1600 px canvas: `1.8–2.6 px`.
- Corner radius: `10–16 px`; rounded rectangle, not pill-shaped.
- Internal horizontal padding: `18–28 px`.
- Internal vertical padding: `14–22 px`.
- Typical node height: `66–96 px`.
- Optional shadow: black at 6–10% opacity, blur `8–14 px`, Y offset `2–4 px`. Omit if the figure is already dense.

### Section/platform header band

- Fill: `#9EDBCB` or a nearby mint.
- Text: `#12233D`, bold.
- Use a shallow header band above a white/light panel for platform or subsystem headings.
- For large research-framework blocks, a soft `#EEF4F5` panel with a mint header is preferred over a fully saturated rectangle.

### Protocol/control card

- Fill: `#F3EEFF`.
- Stroke: `#8B66E8`.
- Text: `#2D2358` or `#12233D`.
- Use for HTTP/MQ protocol inputs, decisions, manual review, optional control states, or explicitly non-data channels.

### Success/output highlight

- Fill: `#EAF7EE`.
- Stroke: `#70B588`.
- Use only for a semantically important validated output or ready state.

### Group/stage boundary

- Fill: none or transparent.
- Stroke: `#82AEEF`.
- Width: `2.2–3.2 px`.
- Dash pattern near `10 8` or `12 9` at 1600 px canvas.
- Corner radius: `18–26 px`.
- Keep at least `22–32 px` clearance from enclosed cards.

### Major pipeline arrow/spine

Use only for pipeline-spine layouts.

- Main fill: `#1F62CA` or a restrained left-to-right gradient `#2A66D5 → #10B9AE`.
- White or very light labels may be used on the saturated spine.
- Do not apply gradient fills to ordinary cards.

## 5. Connectors

- Normal data-flow stroke: `#3F86DF`.
- Normal width: `2.4–3.4 px` at 1600 px canvas.
- Major spine/critical pipeline: `4–6 px` or a filled arrow shape.
- Arrowhead: compact filled triangle matching the connector.
- Routing: orthogonal elbows for stage architecture; straight/simple angled connectors may be used for research-framework or pipeline compositions when they improve clarity.
- Prefer shared horizontal/vertical rails over many independent tangled lines.
- Keep at least `12–18 px` clearance from unrelated text/cards.

Semantic connector colors:

- Blue for normal data/control flow.
- Lavender for protocol/control/decision channels.
- Orange dashed for failure/retry/compensation.
- Teal may be used for secondary data relationships when blue already encodes the major spine.

Avoid decorative curves unless the source topology or the selected research-roadmap layout actually requires them.

## 6. Typography

Recommended fallback stack:

`Microsoft YaHei, Noto Sans CJK SC, Source Han Sans SC, Arial, sans-serif`

At a `1600×900` canvas:

- Figure title if the source contains one: `32–40 px`, weight `800`.
- Major stage/group title: `24–30 px`, weight `750–800`.
- Panel/header band title: `21–26 px`, weight `700–800`.
- Standard node title: `17–21 px`, weight `650–750`.
- Subtitle/annotation: `14–17 px`, weight `500–600`.
- Small connector label: `13–15 px`, weight `500–600`.

Text colors:

- Primary: `#12233D`.
- Secondary: `#566980`.
- White is reserved for labels placed directly on a saturated blue/teal major spine.

Scale text proportionally with canvas dimensions. Do not reduce standard node text below a visually equivalent 16 px merely to fit more content.

## 7. Hierarchy and spacing

- Sibling cards: align edges and keep uniform widths where practical.
- Horizontal sibling gap: roughly `24–42 px`.
- Vertical stage gap: roughly `22–40 px`.
- Major phase separation: `42–72 px`.
- Section title to boundary top: `18–30 px`.
- Keep branch labels close to their connector.
- Use white space and panel grouping to express hierarchy; avoid decorative separators.
- On stage-architecture diagrams, align section headers to one common top baseline and the lower card rows to shared horizontal rails.

## 8. Icons

Icons are optional and should function as semantic markers, not decoration.

- Use simple flat line icons in teal/blue/lavender.
- Keep icon stroke weight consistent.
- Use familiar symbols only: document, checklist, server, database, terminal, shield/check, eye/observation, cloud, user, storage, message/protocol.
- Do not add robots, brains, locks, circuit motifs, or generic “AI” imagery unless the source already requires them.
- If text density is high, omit icons rather than shrinking labels.

## 9. Visual effects

Preferred:

- Flat/light fills.
- Crisp borders.
- Very light shadows only when useful for separation.
- Subtle translucent blue/violet discs or bands only for layered research-roadmap figures.
- One restrained blue→teal gradient on a major pipeline arrow when it matches the selected reference family.

Avoid:

- Dark full-canvas backgrounds.
- Neon glow or bloom.
- Heavy gradients on cards.
- Glassmorphism or frosted panels.
- Texture noise, grid/circuit wallpaper, lens flare, metallic effects, 3D extrusion.

## 10. Document-specific guidance

For competition documents and judges' review:

- Optimize for print/PDF clarity and page-width readability.
- Keep semantic color count low.
- Preserve strong dark-text contrast on light surfaces.
- Prefer vector SVG for text-heavy diagrams.
- Keep images, panels, and labels visually stable when scaled to about 15–17 cm document width.
- If a figure caption is managed by Word/PPT, leave the internal canvas title-free unless explicitly requested.
