# Production Guide

## 1. Inspect And Plan

1. Probe each video for dimensions, frame rate, duration, audio, and rotation.
2. Build a contact sheet or sample frames before cutting. Mark product-only, hand-detail, size/portability, texture, absorption, and CTA shots.
3. Transcribe narration and check the exact beginning and end of every useful spoken sentence. Flag repeated words, repeated short clauses, false starts, and partial syllables.
4. Make one shared cut list for picture and narration, with no repetitions or dead air. Delete every no-voice interval between usable phrases, including pauses inside a single source take. Preserve complete syllables and only a short natural tail. Allocate roughly 4–6 seconds to the hook and 2–5 seconds to supporting shots within a 25–35 second target.
5. For comparable beauty demos, default to 1.2x for both picture and narration while preserving pitch. To prevent accumulated sync drift, derive each beat's target duration from a whole number of output frames, then calculate the pitch-preserving audio tempo from `source_duration / target_duration`; the result should remain close to 1.2x.

The narration is the master timeline. Every silent interval, breath, music-only passage, false start, partial phrase, and repeated word/clause must be removed. Picture and audio for each beat must use the same source in/out points. After editing, read the retained speech from start to finish: every sentence must remain complete, grammatical, and natural. Prefer cutting to suitable B-roll rather than keeping silent footage to bridge a visual change.

## 2. Edit The Picture

- Use only the parts that show a clear product, readable label, clean hand movement, or useful texture.
- Prefer continuity from product reveal to demonstration. Avoid bouncing repeatedly between unrelated angles without narrative reason.
- Keep motion natural. If a shot is static, a subtle 2–5% push-in is enough.
- Use direct cuts only. Do not use dissolves, crossfades, flashes, spins, shake effects, or animated transitions.
- Do not crop through the product or key label text.
- Cut at the end of the last usable syllable. Only incidental boundary audio needed to avoid clipping may remain; no deliberate pause, breath, or music-only interval may remain.
- Do not keep a no-voice interval merely to preserve visual continuity; use a direct picture cut to suitable product or application footage instead.
- When concatenating multiple beats, build video and audio from the shared cut list in one timeline, or verify every temporary segment's duration before joining. Never assemble independently trimmed picture and audio and assume they remain synchronized.

## 3. Build Captions

For Jianying, use a cute rounded handwritten typeface such as Hannotate SC Bold, with white fill and a thick black outline. Do not add a shadow. Place the text block around 71.5% frame height rather than at the default bottom position.

For FFmpeg/libass at 1080x1920, a close mapping is:

```text
Fontname: Hannotate SC
Fontsize: 74
Bold: yes
PrimaryColour: white
OutlineColour: near-black
BackColour: transparent
BorderStyle: outline
Outline: 6–8
Shadow: 0
Alignment: center
Caption centerline: y ≈ 1373
```

Split long narration into short readable phrases. Use yellow only for the product name or one or two emphasized terms. Keep text within roughly 100–980 px horizontally and leave more than 450 px below the caption band for platform controls.

## 4. Compose The Cover

1. Choose a sharp frame or photo where the product is unobstructed and the label is readable.
2. Map the product bounding box before placing text.
3. Group the product name and one short factual selling line in the lower-middle part of the frame. At 1080x1920, use centerlines around `y=1450` for the title and `y=1600` for the selling line.
4. Use Yuppy SC for both lines at 1080 width and start both at **96 px** (HanziPen SC Bold, then Yuanti SC Bold are fallbacks); reduce both equally only if needed to fit.
5. Keep both lines horizontally centered, about 150 px apart. Do not place them above the product or person's head. If needed, move the pair together within the clear lower area to avoid the face, product label, or platform UI.
6. Use white fill and a black outline only. Do not add a shadow. Export a separate 1080x1920 JPG.

## 5. Music And Mix

- Always use `assets/memorable-trip.mp3` — “Memorable Trip” by 陈玖仟 (Kon-Q).
- Set the source music gain to **5%** (`volume=0.05`) before mixing. Apply short opening and closing fades.
- Target a normal streaming mix rather than extreme loudness. Use about -14 to -16 LUFS integrated, with true peak no higher than -1 dBTP.
- Do not distribute the raw audio asset separately from a finished edit.

## 6. Quality Control

- Watch the full video once without pausing.
- Compare final video and audio durations; at 30 fps they must differ by no more than one frame (`0.033` seconds). Spot-check sync near the beginning, middle, and end.
- Confirm no last syllable is clipped by a cut, transition, or end fade.
- Transcribe the final mix and compare it with the retained script.
- Measure the narration stem before adding music with `silencedetect=noise=-35dB:d=0.15`. No editorial pause of 0.15 seconds or longer should remain.
- Confirm no editorial silent interval remains between spoken phrases; only unavoidable syllable-boundary audio may remain.
- Confirm the retained narration is complete, grammatical, and natural at every cut.
- Compare the final transcript with the source: no false start, repeated word, duplicate clause, or duplicated sentence may remain.
- Confirm adjacent visual clips use direct cuts, not transitions.
- Verify captions are centered around the measured height and never cut off at the sides.
- Confirm captions and cover text have no drop shadow.
- Check yellow emphasis does not cover all words indiscriminately.
- Check the cover on a phone-sized preview and at thumbnail scale.
- Check cover title and selling line use the same font and font size.
- Confirm the cover copy remains grouped in the lower-middle area (about 75.5%/83.3% of frame height at 1080x1920) and is not above the product or head.
- Verify product label, captions, and cover text remain readable.
- Decode-check the exported MP4 and confirm H.264/AAC, 1080x1920, normal rotation, and no clipping.
