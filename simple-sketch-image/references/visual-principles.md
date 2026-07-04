# Visual Principles

## Style

- Use a clean white background by default.
- Use black hand-drawn line art as the main visual language.
- Prefer simple shapes, visible logic, and strong whitespace.
- Keep the subject around 40%-60% of the canvas for article body images.
- Avoid heavy rendering, realistic lighting, 3D, gradients, paper texture, shadows, and photo-like output.
- Avoid polished commercial vector illustration unless the user explicitly asks for it.

## Character Library

Select characters by explicit user intent first. Built-in characters are optional helpers, not mandatory mascots.

Default character: `线框人`

Available built-in characters:

- `线框人`: a hollow outline person drawn with a simple continuous line, oval head, tiny hands, thin legs, calm and curious. Best general default for neutral explanations.
- `纸片人`: a folded paper-note figure with a rectangular paper body and one dog-eared corner, simple stick arms and legs. Best for articles, notes, tutorials, documents, and knowledge work.
- `光标人`: a small cursor-arrow headed helper with simple arms and legs. Best for software, AI tools, interaction, selection, and operation flows.
- `印章人`: a rubber-stamp shaped worker with a small handle top, rectangular body, and stick limbs. Best for review, approval, verification, rules, and process control.
- `书签人`: a bookmark-shaped figure with a V notch at the bottom, simple face dots, and thin limbs. Best for reading, article navigation, knowledge bases, and annotation.
- `种子人`: a hollow seed-shaped figure with one small leaf and thin limbs. Best for growth, learning, long-term systems, cultivation, and gradual improvement.

The selected character must perform the core action when used. Do not place it beside the image as decoration.

## User-Defined Character

If the user provides a character description, reference image, brand mascot, or role design:

- preserve the key identity traits the user names
- simplify it into sketch form unless the user asks otherwise
- keep the character consistent across images
- do not invent extra lore, costume, or personality unless needed for the image
- if details conflict with simple sketch readability, keep the most recognizable 2-4 traits

## Character Decision Rules

Use this decision order:

1. If the user asks for no character, use no character.
2. If the user provides a custom character, use that custom character.
3. If the user names a built-in character, use that built-in character.
4. If the user gives no character preference, use `线框人` only when a character makes the idea easier to understand.
5. If a pure object, icon, map, machine, or process explains the idea better, use no character.

Use a character when the concept involves action, struggle, workflow, learning, building, choosing, explaining, or transformation. Do not use more than one character type in a single image unless the user explicitly asks for multiple roles.

## Chinese Label Limits

Default label rules:

- cover image: 0-3 labels
- body illustration: 3-6 labels
- tutorial step image: 3-7 labels
- maximum per label: 2-8 Chinese characters
- avoid full sentences
- avoid paragraphs
- avoid tiny text

If a generated image contains garbled Chinese, reduce label count and regenerate or edit. For important text, consider producing a clean image without text and adding text later with a deterministic design tool.

## Accent Colors

Default is black and white. Use accent colors only when helpful.

- red: warning, error, key tension, important result
- orange: path, motion, process, arrow, transition
- blue: note, feedback, system state, secondary explanation

Use at most 1-2 accent colors per image. Keep accents sparse.

## Forbidden Defaults

Do not default to:

- dense PPT infographic
- formal architecture diagram
- complex flowchart
- realistic UI screenshot
- 3D render
- photo collage
- cute children's illustration
- decorative poster with weak explanation
- full-page handwritten article
- complex background scene
