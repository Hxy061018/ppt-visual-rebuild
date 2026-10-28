# PPT Visual Rebuild

**A Codex skill for polished, beautiful, editable presentations.**

[English](README.md) · [简体中文](README.zh-CN.md)

Make an editable first draft immediately. Review the rendered slides, use image generation to rethink their visual style and layout, then closely reconstruct the selected designs as editable slides.

```text
Editable first draft → GPT visual review → Image-generated redesign
                    → Editable reconstruction → Rendered quality checks
```

## What it does

- Creates a complete first draft instead of stopping at a planning document.
- Reviews every slide in scope; redesigns can cover most or all slides.
- Generates page-specific design references, not just decorative icons.
- Reconstructs titles, text, tables, numbers, diagrams, and connectors as editable objects.
- Preserves specified headers, footers, logos, slide masters, and other fixed elements.
- Checks the final rendering against the source content, selected design, and protected regions.

Illustrations and photos may remain images. A full-slide bitmap is not presented as an editable deck. Original screenshots, quotes, and metrics remain the factual source.

## Choose a language

Both packages implement the same workflow. The English edition translates the **entire skill, prompt templates, checks, and UI metadata**, not just this README.

| Edition | Skill package |
| --- | --- |
| English | [skills/en/ppt-visual-rebuild](skills/en/ppt-visual-rebuild) |
| 简体中文 | [skills/zh-CN/ppt-visual-rebuild](skills/zh-CN/ppt-visual-rebuild) |

## Use

Download an English or Chinese ZIP from [Releases](https://github.com/Hxy061018/ppt-visual-rebuild/releases). Each contains a `ppt-visual-rebuild/` folder with `SKILL.md`, `agents/`, and `references/`.

If you want to install it, copy **one** edition's `ppt-visual-rebuild` folder into your Codex skills directory (typically `~/.codex/skills/`). Both editions have the same skill identifier; do not install both under that identifier. Downloading or cloning this repository does not install anything automatically.

Example invocation:

```text
Use $ppt-visual-rebuild to create a polished presentation from these materials.
First make a complete editable draft, then review the slides, generate visual
redesigns, and reconstruct them as editable slides. Keep the existing headers
and footers and stay within 20 slides.
```

For an existing deck:

```text
Use $ppt-visual-rebuild to upgrade slides 8–16. Preserve the approved content,
headers, footers, and logo. Generate body-layout references for the pages that
need improvement, then closely reconstruct them with editable text and diagrams.
```

## Requirements and scope

This repository contains workflow instructions and reusable prompts, not a PowerPoint rendering engine or an image-generation API. The host must provide editable presentation authoring, rendering, visual inspection, and image generation. The skill uses available presentation and image-generation skills and can call other relevant skills for the initial draft and assets.

No API keys, model names, or machine-specific paths are embedded. If a capability is unavailable, the workflow requires reporting the limitation accurately. Visual review may be performed by the current multimodal assistant; it does not automatically contact a separate GPT service.

The skill does not prescribe one visual theme, add slides without authorization, invent evidence, or change protected template elements. High fidelity is a design target, verified through rendering; pixel-perfect output is not guaranteed.

## Package contents

```text
ppt-visual-rebuild/
├── SKILL.md                       # Workflow and operating rules
├── agents/openai.yaml             # Skill picker metadata
└── references/
    ├── prompts.md                 # Review, redesign, rebuild, and QA prompts
    └── rebuild-checks.md           # Reconstruction and acceptance checklist
```

The packages have been checked with the skill-creator format validator. End-to-end results depend on the host's tools, fonts, renderer, source material, and visual review.
