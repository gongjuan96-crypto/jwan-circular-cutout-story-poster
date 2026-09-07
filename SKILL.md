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
- Default to a vertical 4:5 canvas; use 3:4 when the source benefits from extra breathing room.
- Keep the original photo recognizable and photographic in the main image area.
- Use a clean horizontal division matching the references: the original photo occupies 46–52% of the canvas height and the graphic field occupies 48–54%. Do not compress the photo into a narrow banner or let the lower field become a small footer.
- Use a solid-color lower field with generous negative space.
- Use a content-driven, sparse circle budget; the count is not a fixed count. First select a few meaningful positions in the upper original photo and cover them with small flat solid-color circles. Then repeat a larger, but still sparse, selection of those source-image crops inside the lower solid-color field. The upper photo area normally has fewer solid circles than the lower field has photographic cutouts. For a visually simple source, use only 2–5 upper circles and 4–10 lower circles; increase only when the source genuinely contains many distinct details. Keep at least 5% of the canvas width as an edge safe zone: circles must not touch the canvas edge, and no circle may be clipped by the edge. Vary diameter, spacing, crop position, and visual density; do not arrange them as a grid.
- Keep circles crisp and flat. Do not add drop shadows, bevels, 3D effects, random stock imagery, or unrelated decorative stickers.

## Reference geometry

The reference images depend on proportion and emptiness more than decoration. Treat these as layout constraints:

| Element | Reference-matched rule |
|---|---|
| Main photo | 46–52% of total height; full-width or nearly full-width; clean horizontal lower boundary |
| Lower graphic field | 48–54% of total height; uninterrupted solid color; no gradient or texture overlay |
| Circle diameter | Mostly 1.5–5% of canvas width; use up to 6% only for one or two anchors |
| Circle count | Content-driven, never fixed; usually 2–5 solid circles in the upper photo and 4–10 small source crops below |
| Circle area | The total circle area of the photographic circles in the lower field is about 5–10% of the lower field; preserve the remaining 90%+ as solid-color empty space |
| Edge safe zone | Keep the outer 5% of the canvas mostly empty; circles do not touch the canvas edge |
| Density | Cluster lightly around a few visual paths while preserving large empty pockets; never fill the field uniformly |
| Text block | One compact block in open space, usually 8–18% of canvas width from the nearest circle cluster |

The lower field should read first as a large area of color and only second as a small collection of image fragments. If the circles occupy more than roughly 1/10 of the lower field, reduce their count or size before adding decoration. Never add circles just to reach a target number.

## Visual recipe

1. Identify the strongest visual anchor in the source: person, building, landscape, artwork, or object. Keep it intact in the original photo area unless the user explicitly requests a crop.
2. Select one high-chroma solid background color. If the user gives a color, honor that user-specified color. Otherwise automatically recommend a color by reading the image's dominant hue, warmth, contrast, subject matter, and emotional tone. Warm travel or sunset scenes may suit coral, tomato, terracotta, or orange; bright sky or exhibition scenes may suit lemon yellow or butter yellow; botanical or quiet outdoor scenes may suit grass, sage, or olive green; cool night or water scenes may suit blue, teal, or lavender. Use one dominant color per output and avoid defaulting to coral red when another color creates stronger contrast or narrative fit.
3. Sample the source image into circles. Prioritize meaningful fragments: eyes, hair, clothing texture, architecture, sky, leaves, water, artwork lines, signs, or other details that help the image feel like a memory map.
4. Distribute a small number of circles asymmetrically across the lower graphic field, following the reference rhythm: a few circles near the upper transition, a loose middle spread, and a sparse lower area. Favor small circles and large empty pockets. The exact positions should feel random but balanced, not mathematically scattered and not filled to capacity.
5. Do not place a circle directly on the horizontal division unless it is a deliberate, isolated transition accent. Never let a circle touch the canvas edge. Keep circles away from faces and hands in the original photo area.
6. For a stronger collage effect, add a small number of flat colored circles over the original photo area. These are accents, not substitutes for the sampled cutouts, and must not cover faces or the main subject.
7. Add typography only after the image structure is stable. Use a clean sans-serif style, white on dark/colored areas and black on light areas. Keep copy short: one main sentence plus at most one tiny label or secondary line.
8. Place captions in open negative space, never across a face or the most important landmark. Use generous line spacing and a restrained hierarchy. English micro-copy is suitable for travel, exhibition, diary, and lifestyle images; Chinese copy may be used when requested.

## Caption behavior

If the user supplies copy, reproduce it exactly unless they ask for editing. If no copy is supplied, generate one concise sentence that reflects the source scene, plus an optional two-word micro-label. Do not invent factual locations, dates, names, or claims that are not supported by the photo or the user's brief.

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
- Text is legible, short, and does not obscure the visual anchor.
- The result is a single coherent poster suitable for social sharing.

When using imagegen or another image generation tool, pass the source image as the reference and state these constraints explicitly in the prompt. Prefer precise layout language over generic style labels.
