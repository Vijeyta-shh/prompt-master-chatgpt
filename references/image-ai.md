# Image AI Prompting Reference

First distinguish **generation** from **editing**.

## Generation anatomy

Useful dimensions include:
1. subject
2. environment
3. composition/framing
4. pose/action
5. visual style/medium
6. lighting
7. mood/atmosphere
8. palette/materials/textures
9. camera/lens/depth of field when relevant
10. aspect ratio/output intent
11. exclusions

Prioritize the defining visual facts. Too many competing adjectives can weaken the result.

## Reference-image editing

Explicitly separate:

```text
Change:
- ...

Preserve exactly:
- ...
```

Mention identity, pose, composition, background, typography, lighting, colors, or other elements that must not drift.

## Midjourney

Prefer compact descriptors. A useful order is subject → environment → composition → style → lighting → mood → camera → parameters. Use negative/exclusion parameters only when needed.

## GPT Image / DALL·E-style prompting

Natural-language scene descriptions work well. For complex scenes, describe spatial relationships explicitly: foreground, midground, background; left/right; relative size; where text belongs.

## Stable Diffusion

Keep the positive prompt focused. Use negative prompts when the workflow/model benefits from them. Weighting syntax should clarify priority rather than compensate for a contradictory prompt.

## Text in images

When exact text matters, provide the exact wording, location, hierarchy, capitalization, and style. Do not request extra decorative copy unless desired.
