---
name: simple-sketch-image
description: Generate clean simple-sketch image prompts and images for articles, covers, tutorials, workflows, concept explanations, metaphors, and visual notes. Use when Codex needs to turn a paragraph, article, outline, Markdown file, screenshot text, or user idea into a white-background sketch illustration, including black-and-white line art, optional sparse accent colors, optional fixed character design, Chinese labels with strict text limits, cover images, body illustrations, step-by-step tutorial visuals, or QA and iteration prompts for generated images.
---

# Simple Sketch Image

## Core Purpose

Create simple sketch illustrations that explain text clearly. Prefer white background, black hand-drawn line art, strong whitespace, and a single visible idea per image.

Select characters by explicit user intent first. If the user asks for no character, do not use one. If the user provides a character, brand mascot, reference image, or role description, use that as the fixed character. If the user names a built-in character, use it. If the user gives no character preference, prefer the default `线框人` only when a character helps explain the idea; pure object, icon, map, or process images may use no character.

## Load References

Read only the files needed for the current request:

- `references/visual-principles.md`: style rules, default character, Chinese text limits, color rules, and forbidden styles.
- `references/composition-types.md`: choose image type for covers, article body illustrations, tutorials, workflows, comparisons, metaphors, and explanations.
- `references/prompt-template.md`: generation and editing prompt templates.
- `references/qa-checklist.md`: post-generation review and iteration rules.
- `references/examples.md`: concise examples for body illustration, cover, and tutorial prompts.

Reference selection:

- Read `visual-principles.md` for every image or prompt request.
- Read `composition-types.md` when choosing between cover, body illustration, tutorial, workflow, comparison, metaphor, route, or comic formats.
- Read `prompt-template.md` when writing generation prompts, editing prompts, or shot lists.
- Read `qa-checklist.md` after generating or reviewing an image.
- Read `examples.md` only when the request is ambiguous, the output format is unclear, or a concrete pattern would help.

## Workflow

### 1. Understand the Source

Read the user's paragraph, article, outline, screenshot text, Markdown file, or brief. Extract:

- the core claim or main logic
- the section that most needs a visual anchor
- the intended use: cover, body illustration, tutorial step, explanation, metaphor, or visual note
- whether a fixed character is requested, optional, or forbidden
- whether Chinese labels are needed

For detailed character selection rules, use `references/visual-principles.md`.

Do not illustrate every paragraph by default. Choose only the strongest visual anchor unless the user asks for multiple images.

### 2. Choose the Output Mode

If the user asks for planning, return a concise shot list. For each image include:

- placement or use
- core meaning
- composition type
- character rule
- suggested elements
- suggested Chinese labels

If the user asks to generate images and an image generation tool is available, generate each image separately. If image generation is not available, output a complete copy-ready prompt for another image model.

### 3. Separate Cover and Body Rules

For a cover image:

- make the visual premise clear at first glance
- use one strong central metaphor or scene
- allow more visual contrast than body illustrations
- keep labels very short, or omit labels if the cover should carry external title text

For a body illustration:

- prioritize explanation over impact
- keep the drawing quieter and more spacious
- use 3-6 short labels only when they improve comprehension
- avoid turning the image into a slide, chart, or dense infographic

### 4. Generate or Write the Prompt

Use `references/prompt-template.md` for prompt construction. Include:

- aspect ratio, usually 16:9 horizontal
- white background
- black simple hand-drawn line art
- optional sparse accent colors
- character instructions if relevant
- one core idea
- concrete composition
- strict Chinese label limit
- negative constraints

### 5. Review and Iterate

After image generation, use `references/qa-checklist.md`. Regenerate or edit if:

- Chinese text is garbled or too long
- the image does not explain the source text
- the image is too complex
- it looks like a PPT slide, commercial vector illustration, 3D render, photo, or UI mockup
- the fixed character is missing, inconsistent, or decorative when the user requested it

## Delivery

When generating images, return:

- how many images were generated
- what each image is for
- whether the text passed QA
- which image is strongest and which should be regenerated if needed
- saved path if files are created

When only producing prompts, return the prompt and a short note on how to use it.
