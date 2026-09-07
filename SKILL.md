---
name: circular-cutout-story-poster
description: Use when turning a personal photo into a bold editorial story poster with a complete original photo, a solid-color lower field, and scattered circular cutouts sampled from the source image.
metadata:
  short-description: Create colorful circular-cutout photo story posters
---

# Circular Cutout Story Poster

Create a finished editorial photo poster that treats the original image as a visual memory field: preserve the main photo, divide the canvas with a clean horizontal cut, and let circular source-image fragments reappear inside a contrasting solid-color field.

## Invocation

Use `$circular-cutout-story-poster` followed by one or more source photos. Accept optional instructions for theme, caption, background color, aspect ratio, or whether the subject must remain fully visible.

Example: `$circular-cutout-story-poster，旅行主题，珊瑚红下半区，加入一句简短英文文案。`

## Required output

- Return one single finished image, not separate panels.
- Use a fixed vertical 4:3 format, meaning a 3:4 portrait canvas. Do not switch to 9:16, 4:5, square, or landscape ratios.
- Keep the original photo recognizable and photographic in the main image area.
- Use a clean horizontal division matching the references: the original photo occupies 46–52% of the canvas height and the graphic field occupies 48–54%. Do not compress the photo into a narrow banner or let the lower field become a small footer.
- Use a solid-color lower field with generous negative space.
- Use a content-driven, sparse circle budget; the count is not a fixed count. First select a few meaningful positions in the upper original photo and cover them with small flat solid-color circles. Then repeat a larger, but still sparse, selection of those source-image crops inside the lower solid-color field. The upper photo area normally has fewer solid circles than the lower field has photographic cutouts. For a visually simple source, use only 2–5 upper circles and 4–10 lower circles; increase only when the source genuinely contains many distinct details. Keep circles small by default: most circles should be 1–3% of the canvas width, with no more than one or two anchors reaching 4%. Keep at least 5% of the canvas width as an edge safe zone: circles must not touch the canvas edge, and no circle may be clipped by the edge. Vary diameter, spacing, crop position, and visual density; do not arrange them as a grid.
- Keep circles crisp and flat. Do not add drop shadows, bevels, 3D effects, random stock imagery, or unrelated decorative stickers.

## Reference geometry

The reference images depend on proportion and emptiness more than decoration. Treat these as layout constraints:

| Element | Reference-matched rule |
|---|---|
| Main photo | 46–52% of total height; full-width or nearly full-width; clean horizontal lower boundary |
| Lower graphic field | 48–54% of total height; uninterrupted solid color; no gradient or texture overlay |
| Circle diameter | Mostly 1–3% of canvas width; use up to 4% only for one or two anchors |
| Circle count | Content-driven, never fixed; usually 2–5 solid circles in the upper photo and 4–10 small source crops below |
| Circle area | The total circle area of the photographic circles in the lower field is about 3–7% of the lower field; preserve the remaining 93%+ as solid-color empty space |
| Edge safe zone | Keep the outer 5% of the canvas mostly empty; circles do not touch the canvas edge |
| Density | Cluster lightly around a few visual paths while preserving large empty pockets; never fill the field uniformly |
| Text block | One compact, visually secondary block in open space; use a small 2.5–3.5% of canvas-width letter height and keep it 8–18% of canvas width from the nearest circle cluster |

The lower field should read first as a large area of color and only second as a small collection of image fragments. If the circles occupy more than roughly 1/10 of the lower field, reduce their count or size before adding decoration; the default target is closer to 3–7%. Never add circles just to reach a target number.

## Visual recipe

1. Identify the strongest visual anchor in the source: person, building, landscape, artwork, or object. Keep it intact in the original photo area unless the user explicitly requests a crop.
2. Select one bold solid background color. If the user gives a color, honor that user-specified color. Otherwise automatically recommend a color after analyzing the source photo's dominant hue, warmth, contrast, subject matter, and emotional tone, then favor an artistic color clash: a complementary hue, split-complementary hue, or clear warm-cool contrast instead of a near-identical harmonious color. Examples include pink with teal or cobalt, green with coral or magenta, blue with orange or warm yellow, and muted neutrals with one saturated accent. Keep the clash intentional and readable rather than fluorescent or muddy.
3. Sample the source image into circles. Prioritize meaningful fragments: eyes, hair, clothing texture, architecture, sky, leaves, water, artwork lines, signs, or other details that help the image feel like a memory map.
4. Distribute a small number of small circles as a messy handful across the lower graphic field. Keep them visibly small—usually 1–3% of canvas width—and let the arrangement feel like small balls dropped onto a surface: form one or two irregular mini-clusters with near-touching circles, uneven gaps, and occasional slight overlap; then leave isolated circles far away in other areas. Vary positions strongly in both x and y. Use no equal spacing. The result must look not evenly distributed: avoid symmetry, rows, columns, radial balance, or a tidy grid. Keep large empty pockets and let the visual weight be accidentally unbalanced rather than elegantly centered.
5. Do not place a circle directly on the horizontal division unless it is a deliberate, isolated transition accent. Never let a circle touch the canvas edge. Keep circles away from faces and hands in the original photo area.
6. Add a small number of upper solid circles over the original photo area. Their fill must be the exact same color as the lower solid-color field—same hue, saturation, and brightness—so the upper masks visually connect to the lower panel. These are accents, not substitutes for the sampled cutouts, and must not cover faces or the main subject.
7. Add typography only after the image structure is stable. Use a clean sans-serif in thin or regular weight, white on dark/colored areas and black on light areas. Set the main caption's letter height to about 2.5–3.5% of the canvas width so it remains visually secondary to both the photo and circles. Keep copy short: one main sentence plus at most one tiny label or secondary line.
8. Place captions in open negative space, never across a face or the most important landmark. Prefer a single line; use two lines only when the exact supplied copy cannot remain legible within the safe area. Keep generous breathing room and a restrained hierarchy. English micro-copy is suitable for travel, exhibition, diary, and lifestyle images; Chinese copy may be used when requested.

## Caption behavior

If the user supplies copy, reproduce it exactly unless they ask for editing. If no copy is supplied, generate one concise sentence that reflects the source scene, plus an optional two-word micro-label. Keep the main sentence small, thin, and visually secondary rather than using headline-scale typography. Do not invent factual locations, dates, names, or claims that are not supported by the photo or the user's brief.

## Identity and source fidelity

- Do not redraw, cartoonize, beautify, or materially alter people, faces, products, artwork, or landmarks.
- Every photographic circle must be a crop from the source image; do not hallucinate replacement details inside circles.
- Preserve recognizable colors and textures from the source while allowing the solid field to be graphic and bold.
- If the source is portrait-oriented, protect the face and body silhouette from circle overlays.

## Adaptation modes

| Source | Main area | Circular samples |
|---|---|---|
| Landscape | Keep the horizon and main vista readable | Sky, trees, water, plants, buildings, terrain |
| Portrait | Keep face, pose, and outfit readable | Eyes, hair, fabric, accessories, hands, background texture |
| Exhibition or architecture | Keep the spatial context and key artwork | Lines, frames, lettering, artwork details, walls |
| Everyday record | Keep the atmosphere and dominant action | Small objects, surfaces, light, plants, architectural fragments |

## Quality gate

Before returning the image, verify:

- The main original photo is still immediately recognizable.
- The lower area reads as a solid-color graphic field, not a second unrelated photo.
- Circles visibly contain source-image crops and are not random generated patterns.
- The layout has intentional asymmetry and meaningful negative space.
- The lower circles feel like an accidental scatter: some near-touching, some isolated, with uneven gaps and no repeated spacing pattern.
- Text is legible, short, preferably a single line, and remains visually secondary without obscuring the visual anchor.
- The result is a single coherent poster suitable for social sharing.

When using imagegen or another image generation tool, pass the source image as the reference and state these constraints explicitly in the prompt. Prefer precise layout language over generic style labels.
