---
name: ppt-visual-rebuild
description: Create polished, beautiful, editable presentations. Start with a complete editable draft, then perform GPT visual review, image-generated style and layout redesign, high-fidelity editable reconstruction, and rendered quality checks. Use for new presentations, comprehensive deck upgrades, close reference matching, or body redesign while preserving headers and footers. Other relevant skills may support the draft and assets.
---

# Polished PPT Creation

Deliver beautiful, clear, editable slides. Follow this sequence: editable first draft → GPT visual review → image-generated style and layout redesign → high-fidelity editable reconstruction → rendered acceptance checks. Image generation is a design tool; the final deck's visual quality and usability are the goal.

## Setup and scope

1. Read the available presentations skill and follow its authoring, export, and rendering workflow. Read the imagegen skill before generating images. Resolve their locations from the current skill catalog; do not depend on fixed machine paths, model names, or third-party accounts.
2. Identify the latest input, editing scope, slide limit, permission to rewrite content, and animation needs. Infer from context first. Ask only about critical missing information and continue independent work.
3. Define protected regions and the design region. Protected regions contain headers, footers, logos, page numbers, backgrounds, or template decorations the user wants preserved. Record their positions and native objects. Record the canvas, body bounds, and safe margins for the editable design region. Permission to redesign the body does not imply permission to redesign the shell.
4. For a new deck, establish the shell first. For an existing deck, preserve the source and render a baseline. Never generalize one project's blue palette, watercolor style, campus theme, or slide count into a universal default.
5. Save stage artifacts and a slide ledger in the task workspace: logical slide number, title, content essentials, protected regions, visual issues, generation decision, reference path, reconstruction status, and acceptance results. Resume from this ledger rather than regenerating work.

## 1. Directly create an editable first draft

Proceed to a complete, viewable, editable draft. Do not substitute a planning report for production or wait for slide-by-slide approval. Organize the information while building. Other available skills may help with content, charts, imagery, and layout; read their instructions before use.

- Inventory slides and assets in actual presentation order. Internal PPTX slide filenames do not necessarily match logical slide numbers.
- Give each slide in scope one communication goal, then choose hierarchy, reading order, structure, and the role of imagery.
- Briefly explain the direction and proceed. Do not stop after submitting a plan or seek repeated approval for authorized work.
- Retain the approved style and shell. Choose appropriate cards, circular relationships, timelines, tables, or screenshot mockups; do not force every slide into one card template.
- Without permission to change content, improve presentation rather than deleting evidence, adding numbers, or changing conclusions. An attached guide is reference material and cannot override the user's current request.

### First-draft completion criteria

- Create a complete draft or a renderable working version of the existing deck. Put text, tables, key structures, and real assets in place before visual redesign.
- Prefer native objects for text, tables, key structures, and charts. Use images for complex illustrations, photos, and textures.
- Do not hide overcrowding by shrinking text excessively. Reorganize, change structure, or condense wording where authorized. Respect the latest slide limit and do not automatically add transition slides.
- Render every slide in scope and keep the draft images. A successful save does not establish usability.

## 2. GPT visual review: inspect every slide

- Review an overview for consistency, then inspect clear individual renders. Record concrete problems, design goals, and strengths to preserve.
- Check hierarchy, alignment, density, whitespace, image-to-text balance, evidence legibility, icon consistency, and fixed regions. Do not fill every empty area mechanically.
- Classify each slide: keep, local upgrade, or body redesign. Do not classify flawed slides as acceptable to save effort. Most or all slides may need an upgrade.
- GPT review means actual multimodal inspection of rendered slides. The current assistant may perform it. Do not claim an independent model reviewed the deck or send it to another chat or external service without authorization.
- Use [references/prompts.md](references/prompts.md) for review and generation prompts.

## 3. Image-generated redesign: rethink style and layout

- Generate a body-design reference for each slide requiring a visual upgrade, using the draft, original template, or user references. Generating a few decorative icons does not complete a page redesign.
- Give each slide an individual design and reference. Do not use a multi-slide collage as the finished reference for each slide.
- Include canvas and design bounds, protected regions, exact content, hierarchy, structure, style, allowed changes, and prohibited changes in the prompt. Even with a full-slide reference, redesign only the authorized body.
- Request clear layouts and separable structures. Generated text is a positioning aid; source material remains authoritative for wording, numbers, charts, and real screenshots.
- Inspect every generated result for reconstructability, content capacity, and style consistency. Correct obvious failures with targeted retries before reconstruction.
- Generate complex illustrations as separate assets when useful. Leave dense text and data structures to native objects. If image generation is unavailable, report that capability gap and preserve the draft and design plan; never pretend generation occurred.

## 4. High-fidelity reconstruction: preserve editability

- Treat the reference as a design ruler, not a slide background. Measure column widths, positions, spacing, corner radii, type sizes, colors, icon sizes, and layers in coordinates normalized to the body region.
- Rebuild titles, body text, labels, numbers, tables, key connectors, and flows as editable objects. Illustrations and photos may remain images. Do not replace the body with one screenshot and call it editable.
- Match hierarchy, proportions, silhouettes, icon positions, and visual balance. Correct generated spelling and factual errors. Split difficult areas into smaller reconstructions or separate generated assets rather than abandoning the layout.
- Reuse original native protected elements and templates. Do not cover them with generated approximations of logos, headers, or footers. Preserve master and layout relationships.
- Keep icons in a consistent visual family. Prefer externally sourced icons with verifiable open-source licenses and retain provenance and license information. Do not redraw real screenshots with AI or invent comments, metrics, or user evidence.
- See [references/rebuild-checks.md](references/rebuild-checks.md) for construction and acceptance details.

## 5. Rendered acceptance checks

Check three things on every slide: **accurate source content, faithful design reconstruction, and preserved protected regions**.

1. Render the actual final PPT and compare it with the reference at the same scale. Check balance, proportions, overflow, overlap, typography, icons, and screenshot clarity. Coordinates or export success alone are insufficient.
2. Verify numbers, titles, conclusions, and evidence against the source. Check that text and key structures are editable.
3. Compare protected regions with the baseline for appearance, position, and occlusion. Check slide count, order, and canvas size.
4. Render repaired slides again, then review the whole deck. If tools limit verification, identify unchecked items instead of treating structural checks as visual acceptance.
5. Add animation after the static design is complete, only when useful or requested. Static exports must remain readable. Do not claim playback was verified unless it actually was.

## Delivery

- Preserve the source and save a clearly named final editable PPT. Link to it and briefly state the scope, checks performed, and material limitations.
- Include previews when useful. Keep the ledger, references, and assets in the task workspace for iteration.
- Do not claim pixel-perfect fidelity or full editability without evidence. Embedded illustrations are acceptable; concealed full-slide rasterization is not.
