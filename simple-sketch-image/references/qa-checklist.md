# QA Checklist

## Required

- White background.
- Simple black sketch line art.
- The image explains the source idea.
- One image focuses on one core idea.
- The selected composition type is visible.
- The image is not crowded.
- Chinese labels, if present, are short and readable.
- Default or user-defined character is used only when requested or helpful.
- If a character is used, it performs the core action.
- Accent colors are sparse and purposeful.

## Cover-Specific Checks

- The central metaphor is clear quickly.
- The image can work as an opening visual.
- Labels are minimal or absent.
- There is enough blank area if title text will be added externally.

## Body Illustration Checks

- The image supports the paragraph instead of replacing the article.
- It is quieter than a cover.
- It uses no more than 3-6 short labels by default.
- It avoids slide-like visual density.

## Tutorial Checks

- Steps are visually ordered.
- Each step has one action.
- Text is short enough to read.
- The image does not try to contain the whole manual.

## Failure Signals

Regenerate or edit if:

- Chinese text is garbled.
- text is too long or too small.
- the image looks like a PPT slide.
- the image looks like a commercial vector poster.
- the image is too cute or childish for an explanatory article.
- the image uses gradients, shadows, paper texture, or 3D effects.
- too many arrows, boxes, icons, or labels appear.
- the character is decorative instead of explanatory.
- the visual metaphor does not match the article logic.

## Iteration Rules

- If text fails: reduce labels or remove text and add it later outside generation.
- If explanation fails: rewrite the prompt around one concrete physical metaphor.
- If too complex: remove half the objects and keep one action.
- If too plain: add a stronger object metaphor, not more decoration.
- If too much like a diagram: turn boxes and arrows into a simple scene.
- If character consistency fails: restate only the character's 2-4 key traits.
