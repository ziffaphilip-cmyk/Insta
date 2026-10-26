# Insta: content studio

Planning, scripts, editing style and performance tracking for your Instagram and TikTok reels.
Everything is plain Markdown and CSV, so you can read and edit it on your phone (GitHub app or
github.com) or ask Claude to update it for you.

## What's where

| Path | What it is | Who edits it |
|---|---|---|
| `content/strategy.md` | Positioning, pillars, voice rules, posting rhythm, how to read stats | Claude, after we agree changes |
| `content/ideas.csv` | **Master idea bank.** One row per idea, both formats | Both |
| `content/backlog.md` | Readable list of unpublished ideas (generated from `ideas.csv`) | Nobody: regenerate it |
| `content/calendar.csv` | Every scheduled post with date, format, filming needs, effort and status | Both |
| `content/calendar/` | Readable monthly overview and the detailed weekly plan | Claude |
| `content/briefs/` | Full talking-reel briefs with scripts | Claude writes, you approve |
| `content/templates/` | Blank templates: talking reel, overlay reel, weekly plan | Copy, don't edit |
| `content/tracker.csv` | Performance log, one row per published post | You (or send screenshots) |
| `content/footage.csv` | Library of clips you already have, so overlays can reuse them | You |
| `brand/` | The approved Apricot Hour editing style | Claude |
| `references/` | Reels whose style we studied | |
| `tools/content.py` | Helper commands (below) | |

## The workflow

Every idea moves through five statuses, in both `ideas.csv` and `calendar.csv`:

```
idea → scripted → filmed → edited → published
```

1. **idea**: a row in `ideas.csv`. Hook or overlay text drafted.
2. **scripted**: talking reels have a brief in `content/briefs/` with your input filled in. Overlay text is final.
3. **filmed**: clips captured (batch session or B-roll during training).
4. **edited**: Claude has cut it in the Apricot Hour style; you've approved it.
5. **published**: posted. Add a tracker row 7 days later.

## Your weekly routine (about 2–3 hours total)

| When | What | Time |
|---|---|---|
| **Sunday evening** | Ask Claude: *"plan next week"*. Review the plan in `content/calendar/`, answer any script questions | 20 min |
| **One batch session** (weekend) | Film the next 2–4 talking reels in one go | 60–90 min |
| **During normal training** | Grab the B-roll on the weekly list | 5 min per session |
| **After filming** | Send the clips: *"edit this week's reels"* | 5 min |
| **Posting days** | Pick a sound in-app, post to Instagram and TikTok | 10 min each |
| **7 days after each post** | Log stats in `tracker.csv`, or send Claude an Insights screenshot | 3 min each |
| **End of month** | Ask Claude: *"review the month"*. Claude runs the report and suggests what to test next | 20 min |

## Things you can ask Claude

- "Plan next week" / "Swap Friday's post for something easier"
- "Develop T11" → full script, or a ready-to-post overlay
- "Here's something that happened today…" → Claude judges whether it's a talking reel, an overlay or both, and adds it to the bank
- "This topic feels too broad: …" → Claude finds a sharper angle
- "Here are my stats" (screenshots are fine) → logged, analysed, next experiments suggested
- "Edit these clips" → edited in the house style

## Helper commands

Run from the project folder (Claude can run these for you):

```bash
python3 tools/content.py check          # validate the CSV files
python3 tools/content.py backlog        # rebuild content/backlog.md
python3 tools/content.py week           # what's scheduled this week
python3 tools/content.py week 2026-11-09
python3 tools/content.py report         # performance summary from tracker.csv
```

## Editing the CSV files

- Keep the header row as it is. Blank cells are fine.
- Allowed values: format `talking` / `overlay`; pillar `strength` / `mindset` / `lifestyle` / `opinions` / `relatable`;
  status `idea` / `scripted` / `filmed` / `edited` / `published`; effort `S` / `M` / `L`.
- Numbers in the tracker can be written `12400`, `12,400` or `12.4k`.
- Run `check` after editing by hand; it tells you exactly which line is wrong.

No passwords, logins or paid tools are needed. Stats come from your own Instagram and TikTok insights.
