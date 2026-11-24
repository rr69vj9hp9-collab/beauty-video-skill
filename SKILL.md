---
name: beauty-video
description: Create or edit vertical beauty and skincare product-demo videos in the user's Jianying-derived style, including narration-locked edits with no silent gaps or repeated speech, cute handwritten Chinese captions, black-only outlines without shadows, direct cuts, 1.2x pacing, product-aware covers, and the fixed Memorable Trip soundtrack. Use for cosmetics, skincare, sample showcases, texture demonstrations, and their covers; do not apply this visual style to unrelated travel or general-life videos unless explicitly requested.
---

# 美妆视频

Produce a polished 9:16 product-demo video and cover that feel like a concise Jianying beauty/skincare edit. Reproduce the user's visual signature while adapting shot order and text placement to each product.

## First Pass

1. Inventory every supplied clip and image. Check dimensions, duration, audio, focus, product legibility, and whether people or hands occlude the product.
2. Treat the spoken narration as the master timeline. Transcribe it and mark every non-speech interval, false start, partial syllable, repetition, and incomplete sentence. Build one fluent, complete copy of each idea using only claims supplied in the footage, user copy, packaging, or captions; do not invent efficacy, ingredients, prices, or results.
3. Build one ordered cut list of retained source ranges and use those exact same ranges for picture and narration. Do not create separate picture and audio edit plans.
4. Identify the practical product story: pain point or need, product reveal, size or portability, core benefit, texture/demonstration, then call to action.
5. Read [references/style-analysis.md](references/style-analysis.md) before making creative decisions. For output mechanics and QA, read [references/production-guide.md](references/production-guide.md).

## Video Edit

- **Narration lock:** The spoken narration determines every edit point. Picture follows the narration, not the other way around.
- **Hard A/V sync:** Picture and narration must come from the same cut list and the same source in/out points. Quantize every retained beat to a whole-frame duration, then set both picture speed and pitch-preserving audio tempo from that shared duration. Do not trim picture and narration independently or allow duration drift to accumulate across concatenated clips.
- **No silent gaps:** Delete every interval without usable speech between phrases, including breaths, room tone, music-only passages, and pauses inside a take. Do not retain editorial silence merely to preserve visual continuity. Only unavoidable boundary audio needed to avoid clipping a syllable may remain; it must not sound like a deliberate pause.
- **Keep the sentence coherent:** After every cut, the retained narration must remain complete and flow naturally. Never clip an opening consonant, a final syllable, or a phrase whose meaning depends on removed words. When necessary, trim the neighbouring phrase slightly so the result is grammatical and easy to understand.
- **Deduplicate completely:** Remove repeated words, false starts, repeated short phrases, repeated clauses, and repeated takes. Keep the single cleanest complete instance that makes the spoken sequence coherent.
- Default to 1080x1920, 30 fps, SDR/BT.709. Aim for roughly 25–35 seconds when the script permits.
- For comparable beauty/skincare demos, default to **1.2x** for both picture and spoken narration, preserving pitch. Slow down only when a complete word or sentence needs more room.
- Keep the reference's compact structure: a 4–6 second hook, then 2–5 second product/detail beats, and a short benefit or sample-first close.
- When a phrase needs a different visual, use a direct cut to the closest suitable product, hand, texture, or application shot; never keep silent footage as a bridge.
- Favor product close-ups, clean hand demonstrations, size comparisons, bag/portability shots, texture close-ups, and application proof. Keep the product label readable.
- Use **direct cuts only**. Do not add crossfades, dissolves, flashes, or other visual transitions unless the user explicitly changes this preference.
- Normalize the final mix for clear narration. Background music must support the voice rather than compete with it.

## Caption Signature

The user calls this the “黑皮格式”; interpret it as the visibly established treatment, not a request for a literal black background box.

- Use a cute, rounded handwritten Chinese typeface. Prefer Hannotate SC Bold; Yuanti SC Bold is an acceptable fallback.
- Fill: white (`#FFFEFE`). Outline: near-black (`#070100`). **No shadow.**
- At 1080x1920, use roughly 72–78 px type and a 7 px black outline. Keep the text centered.
- Put the centerline of the subtitle band at about **71.5% of frame height** (`y ≈ 1373` on a 1920-high frame). Do not push captions to the bottom edge.
- Prefer one line. Allow two only when needed, keeping the band centered on the same reference height and within about 86% of the frame width.
- Keep one narration idea per caption and omit unnecessary terminal punctuation.
- Use warm yellow (`#F9E90B`) under the same black outline for the product name and one or two meaningful selling points. A full-line yellow product reveal is acceptable; do not make every caption yellow.

## Cover Style

- Produce 1080x1920 with **Yuppy SC**, a rounded, playful Chinese cover face. If it is unavailable, fall back to HanziPen SC Bold, then Yuanti SC Bold.
- Use white fill, the same black outline treatment, and no shadow.
- Inspect the product position before laying out text. Never cover the bottle, package, product logo, or readable label.
- Use the **same font and same font size** for the primary title and the selling line. At 1080 width, start both at **96 px** unless the copy overflows, in which case reduce both equally.
- Keep both copy lines grouped in the lower-middle part of the frame. At 1080x1920, center the primary title at `y ≈ 1450` and the selling line at `y ≈ 1600`. Do not place cover copy above the product or above the person's head.
- Preserve the lower placement when adapting the layout. If the exact coordinates would collide with the person, product, or platform UI, move the two lines together within the clear lower area instead of splitting them around the product.
- Prefer a one-line primary title. Keep the selling line short and factual. Do not add dates, badges, boxes, or decorative panels unless requested.

## Music

- Always use **“Memorable Trip” by 陈玖仟 (Kon-Q)** for this skill. The user-supplied clean track is stored at [assets/memorable-trip.mp3](assets/memorable-trip.mp3).
- Do not switch to another track or genre unless the user explicitly asks.
- Use **5% of the source track level** (`volume=0.05` before mixing), with a short fade-in and fade-out. Keep the music below the narration; this 5% setting is the user's current default.
- Use the track only for the user's personal edits; do not redistribute the raw audio asset itself.

## Deliver

Provide an MP4 and a separate cover JPG. Transcribe the final mix and compare it with the retained script. Check that the picture and audio durations differ by no more than one frame, and spot-check sync near the beginning, middle, and end. On the narration stem before the music mix, check for silent intervals of 0.15 seconds or longer at `-35 dB`; there should be none except unavoidable syllable-boundary tails. Confirm every retained sentence is complete and coherent, no word or sentence repeats accidentally, captions do not collide with the product or UI-safe areas, no visual transition sneaks in, the cover lines use one shared size, the default soundtrack is Memorable Trip, and the final audio does not clip.
