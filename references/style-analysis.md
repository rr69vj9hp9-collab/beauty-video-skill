# Reference Style Analysis

## Reference Evidence

- Video: 31.57 s, 1080x1920, 39.15 fps, HEVC, stereo AAC.
- Cover: 988x1758, essentially a 9:16 crop.
- Assets:
  - `assets/caption-reference.jpg`
  - `assets/cover-reference.jpg`
  - `assets/sequence-reference.jpg`
  - `assets/final-caption-reference.jpg` — final approved caption style
  - `assets/final-cover-reference.jpg` — final approved cover style
  - `assets/memorable-trip.mp3` — user-selected default soundtrack

These are user-supplied references. Use them to match typography, spacing, and pacing; do not copy a brand claim into a different product.

## Final Approved Style

The `final-*` assets supersede conflicting details in the earlier reference:

- Use cute rounded lettering. Keep Hannotate SC Bold for in-video captions and use Yuppy SC for cover copy.
- Use white fill and a thick black outline with **no shadow**.
- Use direct cuts only; no visual transition.
- Default comparable beauty edits to 1.2x picture and narration speed with pitch preserved.
- Cover title and selling line use the same typeface and same size.
- Keep cover copy grouped in the lower part of the frame rather than above the product or person's head.

## Caption Geometry

Measurements from representative subtitles:

- Black outline bounding box: `y=1333..1413` at 1920 px height.
- Caption center: approximately `y=1373`.
- Center position: approximately **71.5% of frame height**.
- Caption occupies about 4.2% of the frame height.
- Side margins are generally at least about 100 px, with centered text.
- Text is commonly one line; long thoughts can be split, but the whole block stays centered around the reference band.

At other frame sizes:

```text
caption_center_y = frame_height * 0.715
font_size ≈ frame_height * 0.0375..0.041
```

## Typography And Color

- Caption typeface: cute rounded handwriting. Prefer Hannotate SC Bold, then Yuanti SC Bold.
- Cover typeface: use the more playful Yuppy SC. If unavailable, fall back to HanziPen SC Bold, then Yuanti SC Bold.
- White fill median: approximately `#FFFEFE`.
- Yellow emphasis median: approximately `#F9E90B`.
- Black outline median: approximately `#070100`.
- Do not add a drop shadow.
- The black outline is thick and consistent. There is no translucent caption box.
- Product-name reveal lines may be yellow in full.
- Ingredient/benefit lines often use white text with only the most useful phrase in yellow.
- CTA lines are commonly all white.

Preserve the emphasis hierarchy:

1. Product name.
2. One sensory or functional benefit.
3. Supporting context in white.

## Measured Sequence

The transcript and picture content organize into seven clear beats:

| Time | Beat | Purpose |
| --- | --- | --- |
| 0–5.9 s | Seasonal skin concern / dull skin; reveal serum | Problem-to-product hook |
| 6.1–9.3 s | 10 ml sample is easy to try | Reduce trial friction |
| 9.7–13.9 s | Small red bottle fits into a bag | Portability proof |
| 14.2–19.1 s | Fermented camellia and botanical ingredients | Product benefit |
| 19.5–27.5 s | Clear gel texture; spreads, absorbs, no stickiness | Sensory/demo proof |
| 27.6–29.3 s | Try the premium serum | Transition to CTA |
| 29.3–31.1 s | Start with a sample to test the feel | Close |

The cut density is modest: product, hand, bag, texture, and application shots change roughly every 2–4 seconds within those narrative beats.

## Cover Geometry

The original cover used these measurements:

- Primary title bounding box: `y=435..514`; center about `y=474.5` (**27.0%**).
- Bottom selling line: `y=1226..1305`; center about `y=1265.5` (**72.0%**).
- Product sits in the open middle space.
- Both lines are horizontally centered.
- Copy uses the same heavy white-fill/black-outline treatment as the video.
- No caption background, border, badge, or date is present.

The current approved cover uses a slightly higher lower-grouped layout:

- Both lines use Yuppy SC and share the same **96 px** type size at 1080 width.
- Primary title center: approximately `y=1450` (**75.5%** of frame height).
- Selling-line center: approximately `y=1600` (**83.3%** of frame height).
- The lines are horizontally centered, about 150 px apart.
- Cover text stays below the product and the person's head, never above them.
- Neither line has a shadow.

The latest cover typography preference above supersedes the older font appearance in `assets/final-cover-reference.jpg`; keep the reference for composition and placement only.

Use these proportions as the default. If the exact position collides with the person, product label, or platform UI, move both lines together within the clear lower area rather than returning them to the top or splitting them around the product.

## Audio

- The recording contains a female Mandarin product narration plus continuous background music.
- Narration remains primary and fully intelligible.
- Final default music: **“Memorable Trip” by 陈玖仟 (Kon-Q)**.
- The clean track is bundled at `assets/memorable-trip.mp3`.
- Mix it at **5% of the source track level** (`volume=0.05`), with short front and back fades.
- Do not substitute another track unless the user explicitly changes this preference.
- During narration cleanup, repeated words or whole repeated clauses must be collapsed to one fluent instance.
- Remove every interval with no spoken voice between phrases. Preserve only a natural syllabic tail, generally under 0.15 seconds, and continue the picture with a direct cut.

## Copywriting Implications

Use short, spoken-language benefit lines. The reference alternates:

- concern or context
- concrete product detail
- sensory outcome
- usage/demonstration proof
- low-risk call to action

Keep product facts tied to the supplied material. Rewrite for brevity when needed, but never add unsupported efficacy claims.
