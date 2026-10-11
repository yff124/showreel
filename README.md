# showreel

Spec portfolio page: [yff124.github.io/showreel](https://yff124.github.io/showreel/)

**What this is.** An AI-generated 16-second film (three shots, 16:9), a separately composed 9:16 social cut, and the pipeline that produced them — built to answer a real question from a hiring manager rather than to pad a résumé.

## Contents

| File | What it is |
|---|---|
| `index.html` | The page. Single file, no external dependencies, no fonts or JS to fetch. |
| `media/film_16x9.mp4` | The cut: 3 shots, 16.1s, 1080p source / 720p web, 24fps, model-native ambient audio. |
| `media/shot1..3.mp4` | The individual shots, in order. |
| `media/shot4.mp4` | The vertical 9:16 cut, composed as a vertical rather than cropped. |
| `media/poster*.jpg` | Still frames pulled for thumbnails and posters. |
| `_raw1080/` | Untouched 1080p generations. Git-ignored; kept locally only. |

## How it was made

1. Nothing written down but a one-line brief.
2. Look locked **before** rendering — palette, lens, light direction, grain and camera behaviour written once and repeated verbatim across all four prompts. This is what makes consecutive shots read as one world.
3. Four text-to-video generations, 1080p, 24fps, native audio kept.
4. Hard cuts, 0.6s fade in, 0.8s fade out, matched audio fades.
5. Delivered for both frames: 16:9 master and a separately composed 9:16 cut.

## Disclosure

Every frame is AI-generated and human-directed. Nothing is presented as live-action footage, and no stock material is used. There is no music bed: the ambience comes with the clips, because shipping audio without a licence is not something this project does.

Re-encoded from the 1080p masters with `ffmpeg` (H.264, CRF 24–25, `+faststart`) so the page loads on a phone without a 30 MB download.
