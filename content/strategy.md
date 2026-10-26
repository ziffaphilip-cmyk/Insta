# Content strategy

The working rules for what we post and why. Update this when the data tells us something new;
log the change at the bottom so we remember why.

## Positioning

**A real woman who lifts, works a corporate job, and has opinions about both.**
People follow for your perspective and personality, not for workout programs. Strength training is
the anchor, and life is allowed to be its own subject.

What makes the account distinct (lean into these):
- **The corporate + lifting crossover.** Most fitness accounts are full-time creators or coaches. You live
  the 9-to-5 reality your audience lives.
- **Honest over polished.** Failed reps, boring sessions and unresolved feelings are content.
- **Observations, not instructions.** You notice things people feel but haven't put into words.

Who it's for: women, mostly 20s to early 30s, who lift or want to, often with full-time jobs, and who
are tired of both hustle-culture and "dream body" fitness content.

## Content pillars

| Pillar | What it covers | Typical goal |
|---|---|---|
| `strength` | Lifting, gym confidence, myths, progress, training realities | saves, reach |
| `mindset` | Confidence, comparison, self-doubt, trying new things | shares |
| `lifestyle` | Work + training balance, routines, small wins, struggles | connection, reach |
| `opinions` | Fitness culture, body image, expectations of women, life lessons | comments |
| `relatable` | Gym humour, POVs, observations people send to friends | shares, reach |

Not every life post has to connect back to fitness.

## The two formats

**Talking reels** (30–60 s, longer only if the topic needs it): build trust and a recognisable point of view.
One clear idea per video. Strong first line, a real middle, a conclusion that isn't a slogan.
Template: `templates/talking-reel.md`.

**Overlay reels** (5–12 s): quick to make, built to be felt in one read. One to three short lines.
Template: `templates/overlay-reel.md`.

Both get edited in the approved Apricot Hour style (`brand/BRAND.md`).

## Starting mix (adjust once data comes in)

Per week: **4 posts + 1 optional**.
- 2 talking reels (Wednesday, Saturday)
- 2 overlay reels (Monday, Friday)
- 1 optional overlay (Sunday) if you have the energy or a trend fits

Across a month, aim roughly for:
- ~40% fitness/strength-anchored (`strength` + gym `relatable`)
- ~20% lifestyle, ~20% mindset, ~20% opinions
- Goals spread across reach, shares, saves, comments and connection, never all one kind
- 1 experimental post every 2 weeks (new topic, hook style or format), labelled `experiment` in calendar notes

Rules:
- No two posts with essentially the same message in the same week.
- Related ideas (e.g. T01 intimidation → T16 practical follow-up) sit 2–4 weeks apart.
- Post the same video to Instagram and TikTok. Remove watermarks; use each app's own text for the caption.

## Voice

**Do:**
- Open with a specific line that makes sense instantly, spoken naturally.
- Use plain words you'd say to a friend. Short sentences.
- Make one honest observation and back it with a specific detail.
- Let some posts end without a lesson.
- Keep captions short when the video already says it.

**Avoid:**
- "Have you ever noticed…", "Here are 5 tips to change your life", "POV: you finally…" templates used lazily
- Empty motivational quotes; "discipline over motivation" variants
- Coach-speak, corporate polish, manufactured controversy, engagement bait ("comment YES if…")
- Health, training or nutrition claims without solid evidence. When in doubt, describe your experience
  instead of making a general claim.
- **Invented personal stories.** If a script needs your experience, it gets a `[bracket]` and I ask you first.

## Hooks that fit your voice

- A specific, slightly surprising statement: "2.5 kilos is a real amount."
- A flipped expectation: "I've been trying to get bulky on purpose for [X] years."
- A real phrase people hear: "'You look like you lift.'"
- A contrast between your two worlds: "At work I'm expected to know the answer. In the gym, failing a rep is the plan."

## Recurring series (light structure without repetition)

- **Progress that doesn't show in photos** (overlay): one everyday proof of strength each time.
- **Signs you've been lifting a while** (overlay): insider jokes.
- **Corporate by day** (overlay or talking): the work + gym crossover.
- **Things I'd tell myself in week one** (talking): one honest thing per video, never a list.

Use a series at most once every 2–3 weeks so it stays a treat.

## Audio

Trending sounds change weekly, so I don't claim something is trending unless it's been checked live.
In the idea bank, audio notes are **search directions**, not claims.

How to find a fitting sound in 5 minutes:
1. **Instagram:** in the Reels editor, open audio and look for the small upward arrow (trending). Save 3–5 that fit the mood.
2. **TikTok:** check the Creative Center's trending sounds list (business/creator view) or the "Trending" tab when adding a sound.
3. Choose by mood first (funny, confident, reflective), then by whether a beat drop lines up with your text.
4. Add the sound inside the app before posting so it's licensed. I edit to a matching tempo and you swap the audio in-app.

Talking reels: no music, or a very quiet instrumental bed under your voice (music ducked 12 dB).

## Measuring

Log each post **7 days after publishing** in `tracker.csv`, then run `python3 tools/content.py report`.

How to read it:
- **Reach (views, non-follower %):** which topics introduce you to new people.
- **Shares per 1k views:** "I felt that" content. Best signal for overlay reels.
- **Saves per 1k views:** useful content people want to come back to.
- **Comments per 1k views:** conversation starters.
- **Follows per 1k views:** what turns viewers into followers. The most important number long term.
- **Average watch % / time:** whether the hook and pacing held people.
- **Feel (1–5):** how it felt to make. A format you hate making won't last, however well it performs.

Compare talking reels with talking reels and overlays with overlays. A talking reel with fewer views but
high follows per 1k is doing its job. Until 8+ posts are logged, every pattern is a hypothesis.

## Month 1 experiments

1. **Hook style:** statement hooks (T01, T07) vs funny flipped hooks (T06, T19). Which holds watch time?
2. **Corporate crossover:** do O04/O18/O27/T20 earn more follows per 1k than pure gym posts?
3. **Overlay length:** one line (O04) vs list format (O03, O21). Which gets more shares?

## Change log

- 2026-10-26: Initial strategy. Instagram profile not yet reviewed (instagram.com blocked in the editing
  environment); revisit once you share screenshots or allow access.
