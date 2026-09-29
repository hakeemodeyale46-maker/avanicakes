# Metrics Glossary

Exact meanings matter. Many bad diagnoses come from misreading a metric. When a user gives a
number, map it to one of these and note which funnel stage it describes.

## Funnel stages and their metrics

| Stage | Question | Main metrics |
|---|---|---|
| Distribution | Was it shown? | Impressions, reach, For You / Browse / Suggested traffic |
| Packaging | Was it chosen? | Impressions CTR, Shorts "viewed vs swiped away", TikTok early hold |
| Hook | Did they stay past the start? | Retention at 0:30 (long) / 0:03 (short), "intro" key moment |
| Body | Did they keep watching? | Retention slope, dips, AVD, APV |
| Payoff | Did the ending land? | End retention, late cliffs, loops/rewatches, "watched full video" |
| Satisfaction | Was it worth it? | Engagement per view, subs per view, shares, saves, returning viewers, long-tail growth |

## Core definitions

- **Impressions** — times the thumbnail/video was shown to someone (definitions vary; YouTube
  counts thumbnail shown on-screen for ≥1s at ≥50% visible, only on YouTube surfaces).
- **Impressions CTR** — views from impressions ÷ impressions. Only covers YouTube surfaces;
  external traffic (links, embeds) is excluded. CTR naturally *falls* as a video is shown to
  colder audiences — a falling CTR alongside rising impressions is usually healthy expansion,
  not failure.
- **Views** — platform-specific. YouTube long-form: a counted play. YouTube Shorts: counts
  starts/replays (engaged views is separate). TikTok/Reels: typically any start, including
  loops. Never compare raw views across platforms as equal.
- **Average view duration (AVD)** — total watch time ÷ views. Absolute seconds/minutes.
- **Average percentage viewed (APV)** — AVD ÷ video length. Compare only across videos of
  similar length; APV naturally drops as length increases.
- **Absolute audience retention** — at each moment, % of views still watching (relative to
  the number of views). Can exceed 100% where people rewind/rewatch or loop.
- **Relative audience retention** — how this video's retention at each moment compares to
  YouTube videos of similar length ("above average / average / below average"). Good for
  judging overall quality without length bias.
- **Key moments (YouTube)** — Intro (first 30s retention), Top moments/spikes, Dips,
  Continuous segments. Use them as bookmarks; still verify against the curve.
- **Viewed vs swiped away (Shorts)** — % of people who saw the Short in the feed and did not
  swipe away immediately. This is the Shorts equivalent of CTR+hook combined.
- **Watched full video % (TikTok)** — % of views that reached the end. Strong completion
  signal.
- **Average watch time (TikTok/Reels)** — like AVD.
- **Skip rate / hold rate (Reels, some tools)** — % leaving in the first ~3 seconds, and its
  inverse.
- **Rewatches / loops** — views that replay. For shorts, loops push retention above 100% and
  are a strong positive signal when they come from genuine rewatching.
- **Unique viewers** — estimated distinct people. Views ÷ unique viewers = views per viewer.
- **Returning vs new viewers** — returning viewers watched the channel before. A video
  reaching many new viewers is breaking out; one only reaching returning viewers is serving
  the existing base.
- **Traffic sources** — Browse (home feed), Suggested (next to/after other videos), Search,
  Shorts feed, Channel pages, External, Notifications, Playlists, Direct/unknown. Each has a
  different viewer mindset (see `human-attention.md`).
- **Engagement rate** — (likes + comments + shares + saves) ÷ views. Shares and saves
  usually matter more than likes: they signal "valuable enough to act on".
- **Subscribers gained per 1,000 views** — satisfaction + "want more" signal.
- **End screen / card CTR** — how many people wanted the next video. High = strong session
  value.
- **Watch time** — total hours. Matters for monetization thresholds and long-form
  recommendation; driven by views × AVD.

## Common misreadings to catch

1. **Treating a low CTR as a failure when impressions are huge.** A 3% CTR on 2M impressions
   can be a massive success. Compare CTR at similar impression levels / time since publish.
2. **Comparing APV across different lengths.** A 50% APV on a 20-minute video is very
   different from 50% on a 40-second Short.
3. **Reading a single bump in a 60-view video as meaningful.** It's one or two people.
4. **Ignoring video age.** Day-1 metrics are dominated by subscribers/core fans; day-30
   metrics include colder audiences. Always note when the data was pulled.
5. **Blaming retention for a distribution problem.** If impressions are tiny, the platform
   barely tested it — retention may be fine.
6. **Reading >100% retention as an error.** It's rewinds/loops. Find what they rewatched.
7. **Assuming views = people.** Replays and loops inflate views, especially on short-form.
8. **Confusing the viewer's reason to leave with the moment they left.** The cause is often a
   few seconds *before* the drop (people decide, then swipe). Look 2–10s earlier.
