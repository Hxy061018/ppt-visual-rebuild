# Reconstruction and quality checks

## Coordinates and protected regions

Record canvas dimensions and body bounds. For body `(x0,y0,w,h)` and a reference position normalized to that body as `(u,v)`, map to `(x0+u*w,y0+v*h)`. Convert units consistently rather than estimating each object separately.

Protected regions may vary by slide: section, content, and closing slides need not share one shell. Record authorized exceptions. Keeping headers and footers does not prevent body edits, and does not mean retaining their words while arbitrarily moving the logo.

## Construction layers

1. Native shell, background, and master relationships.
2. Body silhouettes: columns, cards, rings, tables, flows, and image placeholders.
3. Source content and real evidence; check reading order.
4. Illustrations, icons, image crops, shadows, and decoration.
5. Baselines, padding, type sizes, connection points, and object order.

Prefer native combinations for circular relationships, arrow-shaped cards, and timelines. Complexity alone is not a reason to rasterize them. Textures or complex silhouettes may be backing images while text and key structures remain editable.

## Common failures

| Failure | Remedy |
| --- | --- |
| Attractive reference cannot fit the content | Preserve facts, reorganize blocks, and regenerate if needed; do not force tiny text |
| Generated text or numbers are wrong | Replace them natively from the source; generated images are not factual sources |
| Screenshot metrics are too small | Retain the screenshot, enlarge a real crop, and add native callouts; do not redraw with AI |
| Icons are inconsistent | Unify icon family, stroke, fill, backing circles, and size |
| Flat shapes acquire gradients or 3D effects in the player | Inspect inherited theme effects and style references; set fills and effects explicitly, then render |
| Logo is distorted | Preserve aspect ratio and inspect cropping; do not stretch |
| Validator reports pre-existing source problems | Separate baseline issues from new defects; do not alter protected slides to remove old warnings |
| Internal filenames differ from presentation order | Read the presentation's actual slide relationships and logical order |
| Comment screenshots are duplicates | Verify duplicates, do not count them as independent evidence, and deduplicate by display value |

## Acceptance evidence

- Draft renders, a slide ledger, actual generated references, and final renders exist.
- Every slide in scope was reviewed; reconstructed slides were individually compared with the selected references.
- Titles, conclusions, numbers, charts, and real evidence were checked against the source.
- Protected regions match the baseline; count, order, and canvas meet the latest requirements.
- No unintended overflow, cropping, occlusion, image distortion, or unreadable small text remains.
- Text and key structures are editable; images serve appropriate asset roles.
- Inspect actual PowerPoint rendering where available; with other renderers, watch for font and effect differences.
- Preserve the user's running apps; do not close their windows or quit applications merely to render.

## Example ledger

| Logical slide | Goal | Protected regions | Problem | Decision | Reference | Reconstruction | Acceptance |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 07 | Explain two growth loops | Header 0–9%, footer 95–100% | Empty sides, unclear relationship | Body redesign | references/p07.png | Native three-column layout + illustration | Source wording pending |

Keep ledgers and stage files in the task workspace, not the skill package. Record the selected references and assets to avoid regenerating them after resuming.
