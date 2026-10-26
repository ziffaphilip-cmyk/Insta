# Apricot Hour: reel house style

Status: **DRAFT, awaiting approval.** Do not treat as binding until this line says APPROVED.

Learned from `references/ref-1.mp4`, `ref-2.mp4`, `ref-3.mp4` (lifestyle "day in the life" reels).
Keep their storytelling habits; never copy their fonts, colours or text animations.

## Format
- 1080x1920, 30 fps, H.264 High 16 Mbps, AAC 320 kbps, `-movflags +faststart`
- Length 8–15 s by default, up to 30 s for tutorials/splits
- Also export a clean (no text) copy

## Fonts (files in `brand/fonts/`, SIL OFL)
| Role | Face | Size @1080w | Notes |
|---|---|---|---|
| Hook title | Fraunces 560, SOFT 100, opsz 144 | 104–118 px | lowercase, 2 lines max, tracking −2% |
| Title accent word | Fraunces Italic 480, Apricot | same | exactly one word per title, hand-drawn underline |
| Title subline | Bricolage Grotesque 500 | 40 px | Fog, tracking +4% |
| Chapter time | Fraunces Italic 500, Apricot | 76 px | e.g. `8:12 am` |
| Chapter label | Bricolage Grotesque 560 | 44 px | Milk |
| Caption | Bricolage Grotesque 640 | 58 px | 2–5 words, one key word Apricot 700 |

## Colours
- Milk `#FFF7EC`: all main text
- Apricot `#FF9E5E`: one accent per text block (title word, caption word, time), underline
- Fog `#EADFD1`: sublines
- Espresso `#2A1D16`: shadow only. `text-shadow: 0 2px 22px rgba(42,29,22,.62), 0 2px 6px rgba(42,29,22,.45)`
- Never put text on a coloured box.

## Layout (safe zones, % of 1920 height)
- Keep clear: top 220 px, right 150 px, bottom 340 px; side margin left 96 px
- Chapter band 12–22% · Title band 27–47% (moves to 18–35% if it would cover a face) · Captions 61–73%

## Motion
- Title words: rise 24 px + blur 10→0 + fade, 7 frames each, 4-frame stagger, ease-out
- Underline swash under accent word draws over 10 frames as the last word lands
- Title holds still 3–4 s while 3–5 clips cut underneath; fades out over 6 frames on a beat
- Captions: hard swap on beat with 3-frame fade. No bounce/scale/typewriter
- Chapter marker: 5-frame fade in on the chapter's first cut, holds for the chapter
- Camera: slow 100→104% push only on holds > 1.5 s. No shake, spins, glitches
- Transitions: straight cuts; one 4-frame warm flash dip allowed per reel at a chapter change

## Pacing
- Hook shot hold 1.2–1.6 s, then 0.5–1.0 s shots cut on the beat (refs average ~0.8 s)
- Nothing on screen under 0.5 s
- End on a question line over a shot that matches the opener so it loops

## Grade (FFmpeg)
```
eq=contrast=0.96:saturation=1.06:gamma=1.02,colorbalance=rs=0.03:bs=-0.03:rm=0.02:bm=-0.02:rh=0.02:bh=-0.04,curves=all='0/0.035 0.5/0.51 1/0.975'
```

## Sound
- One music track: mellow R&B / lo-fi / soft pop instrumental, 85–110 BPM; cuts on beat
- Trending/licensed sounds are added by the user in the Instagram app
- Master −14 LUFS integrated, true peak ≤ −1 dBTP (`loudnorm=I=-14:TP=-1:LRA=7`)
- Voice present: duck music −12 dB under speech
- Only SFX: soft paper tick at −28 dB when the underline draws

## Pre-delivery checklist
- Text inside safe zones; one accent per block; nothing < 0.5 s
- First frame works as the cover; ending loops
- Loudness verified at −14 LUFS
