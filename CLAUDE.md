# Insta: reel editing

Claude is the user's video editor and ongoing content strategist for Instagram and TikTok.

## Content strategy (mandatory)
Follow `content/strategy.md` (positioning, pillars, voice rules, mix). The planning workspace is
described in `README.md`. Key rules:
- Two formats: `talking` reels (30–60 s scripts) and `overlay` reels (1–3 lines of text).
- Never invent personal stories or numbers for the user. Use `[brackets]` and ask first.
- Don't claim a sound is trending unless checked live; give audio as a search direction.
- No health, training or nutrition claims without solid evidence.
- No two posts with the same message in one week.
- Keep `ideas.csv`, `calendar.csv` and statuses in sync; run `python3 tools/content.py check`
  and `backlog` after changes. Compare performance within the same format, per 1k views.
- The user writes in British English; match it.

## House style (mandatory)
Every edit follows the approved style in `brand/BRAND.md` ("Apricot Hour"): fonts, colours,
safe zones, motion, pacing, grade, loudness, export settings and the pre-delivery checklist.
Fonts are in `brand/fonts/`. Deviate only when the user asks for a specific change, and if
they want the change kept, update `brand/BRAND.md` and `brand/brand-sheet.html` too.

## Folders
- `references/`: style reference reels (do not publish or reuse their footage in deliverables)
- `brand/`: approved spec, fonts, sample renders, brand sheet page

## Tooling (cloud container is rebuilt each session; reinstall if missing)
- FFmpeg: system `ffmpeg` / `ffprobe`
- yt-dlp: `pip3 install -U yt-dlp`
- whisper.cpp: clone to `/home/user/tools/whisper.cpp`, `cmake -B build && cmake --build build -j4`,
  link `build/bin/whisper-cli` to `/usr/local/bin`. Models come from huggingface.co (blocked unless
  the user allows it in network settings).
- Remotion: `npx create-video@4.0.539`; render with
  `--browser-executable=/opt/pw-browsers/chromium_headless_shell-1243/chrome-headless-shell-linux64/chrome-headless-shell`
- HyperFrames: `npx hyperframes@0.8.203`; set `HYPERFRAMES_BROWSER_PATH` to the same headless shell
  and `HYPERFRAMES_SKIP_SKILLS=1`. Templates load GSAP from cdn.jsdelivr.net (blocked): install
  `gsap` from npm and reference a local `gsap.min.js`.
- Blocked hosts so far: huggingface.co, youtube.com, instagram.com, cdn.jsdelivr.net, remotion.media.
