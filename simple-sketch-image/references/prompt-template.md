# Prompt Templates

## Single Image Generation

```text
Generate one standalone {aspect_ratio} simple sketch illustration for {use_case}.

Style:
Clean pure white background. Minimalist black hand-drawn line art. Simple shapes, slightly human pen lines, strong whitespace, clear explanatory composition. Optional sparse accent color only if useful. No gradients, no shadows, no paper texture, no 3D, no photo realism, no complex background, no polished corporate vector art, no PPT slide look, no dense infographic.

Source idea:
{summary_of_article_or_paragraph}

Image purpose:
{cover / body illustration / tutorial step / workflow / metaphor / explanation}

Core logic to explain:
{one_core_logic}

Composition type:
{composition_type}

Character rule:
{no character / use default character 线框人 because it helps explain the action / use built-in character: 纸片人, 光标人, 印章人, 书签人, or 种子人 / use user-defined character: ...}

Composition:
{concrete scene: where the main objects are, what action happens, how the idea is visually explained}

Suggested visual elements:
{element_1} / {element_2} / {element_3} / {element_4}

Chinese handwritten labels:
{0-7 short labels, each 2-8 Chinese characters; omit if not needed}

Accent color use:
{black and white only / red for ... / orange for ... / blue for ...}

Constraints:
One image explains one idea. Keep the main subject readable and not crowded. Use large empty white areas. If Chinese labels are used, keep them short and legible. Do not invent long text. Do not include garbled characters. Do not write a large title unless explicitly requested. Do not make the image a formal chart, course slide, UI screenshot, or decorative poster. The image should be understandable within one second and still feel hand-drawn.
```

## Shot List Planning

Use when the user asks for illustration planning, article visual strategy, or multiple candidate images before generation.

```text
Shot list for {article_or_topic}

1. Placement:
   {where this image appears, such as cover, after section 2, or tutorial step 1}
   Purpose:
   {cover / body illustration / tutorial step / workflow / metaphor / comparison / comic}
   Core idea:
   {one sentence explaining what the image should make clear}
   Composition type:
   {one type from composition-types.md}
   Character rule:
   {no character / default 线框人 / selected built-in character / user-defined character}
   Visual metaphor:
   {physical scene or object that explains the abstract idea}
   Suggested elements:
   {3-5 objects or visual parts}
   Chinese labels:
   {0-7 short labels, each 2-8 Chinese characters}
   Risk to watch:
   {garbled text / too dense / too PPT-like / weak metaphor / character inconsistency}
```

Keep shot lists concise. Default to 1-3 images for short text, 4-8 for long articles, and avoid turning the article into a picture book unless the user asks for it.

## Built-In Character Inserts

Use only the selected character insert.

```text
Default character:
线框人, a hollow outline person drawn with a simple continuous black hand-drawn line, oval head, tiny hands, thin legs, calm curious expression. 线框人 must perform the key action that explains the idea, not stand beside the drawing as decoration. Keep it neutral, simple, and not cute.
```

```text
Built-in character:
纸片人, a folded paper-note figure with a rectangular paper body, one dog-eared corner, simple stick arms and legs, quiet practical expression. 纸片人 must perform the key action that explains the idea, not stand beside the drawing as decoration.
```

```text
Built-in character:
光标人, a small cursor-arrow headed helper with simple arms and legs, like a thinking pointer, clean and not UI-heavy. 光标人 must perform the key action that explains the idea, not stand beside the drawing as decoration.
```

```text
Built-in character:
印章人, a small rubber-stamp shaped worker with a rectangular stamp body, tiny handle top, stick limbs, serious worker feeling. 印章人 must perform the key action that explains the idea, not stand beside the drawing as decoration.
```

```text
Built-in character:
书签人, a bookmark-shaped figure with a V notch at the bottom, simple face dots, and thin limbs, suited to reading and annotation. 书签人 must perform the key action that explains the idea, not stand beside the drawing as decoration.
```

```text
Built-in character:
种子人, a hollow seed-shaped figure with one small leaf and thin limbs, calm and thoughtful, not cute. 种子人 must perform the key action that explains the idea, not stand beside the drawing as decoration.
```

## User Character Insert

Use when the user provides a character:

```text
Fixed character:
Use the user's provided character as the recurring figure. Preserve these key traits: {traits}. Simplify the character into clean black sketch line art while keeping it recognizable. The character must participate in the core action when present.
```

## Garbled Text Fix

```text
Edit the image to remove or replace the unreadable Chinese text. Keep the drawing, composition, white background, line style, character, and visual logic unchanged. Use only these short readable labels: {labels}. Do not add any other text.
```

## Simplify Overcrowded Image

```text
Regenerate the illustration with the same core idea but fewer elements. Keep only one main metaphor, 3-5 visual elements, and at most {label_count} short Chinese labels. Increase whitespace. Remove decorative details and avoid PPT infographic style.
```
