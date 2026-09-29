# Low-View vs High-View Analysis

The same graph means very different things at 80 views and at 800,000. Always decide how much
to trust the data before interpreting it.

## How noisy is a retention percentage?

Retention at a moment is a proportion. Its rough 95% margin of error is:

```
± 1.96 × sqrt( p × (1 − p) / n )
```
where `p` = retention at that moment (e.g., 0.5) and `n` = views.

| Views (n) | Margin at p = 50% | What you can read |
|---|---|---|
| 30 | ± ~18 points | Almost nothing from the curve |
| 100 | ± ~10 points | Only the biggest shape (huge hook loss or not) |
| 500 | ± ~4.5 points | Hook drop, overall slope, large cliffs |
| 1,000 | ± ~3 points | Specific dips of ~5+ points |
| 10,000 | ± ~1 point | Fine detail, small dips, spikes |
| 100,000+ | < ± 0.5 point | Nearly everything; segment by source/device |

(Rough guide — the viewer pool isn't a perfect random sample, and platforms smooth curves.)
Use this to label each finding with confidence and to avoid over-reading bumps.

## Regime playbooks

### Micro (< ~100 views)
The curve is a handful of people. Don't diagnose timestamps from it.
Do this instead:
1. **Packaging-first**: is the title/thumbnail clear, specific, and desirable at phone size?
   Is the topic something people actually want (search demand, trends, competitor results)?
2. **Content audit**: full simulated-viewer pass. Predict drops from the content itself.
3. **Hook audit**: first 3s (short) / 15s (long) scrutinized line by line.
4. **Aggregate across videos**: combine the creator's last 5–20 videos. Patterns in APV,
   first-30s retention, and CTR across videos are far more reliable than one video.
5. **Qualitative signals**: any comments, what people say, shares.
6. **Distribution check**: if impressions are tiny, the platform hasn't tested it. This is
   often a channel-level issue (consistency, topic clarity, packaging) not a video issue.
7. State plainly: "At this view count the retention graph is too noisy to pinpoint drops.
   This analysis is based mainly on the content and packaging."

### Low (~100–1,000)
- Read the **overall shape** (cliff-then-flat, steady slide, etc.) and the hook drop.
- Treat dips < ~10 points as unconfirmed.
- Lean heavily on the simulated-viewer pass and use data to confirm/deny its predictions.
- Compare to the creator's own average for context.

### Medium (~1,000–10,000)
- Dips of ~5+ points are real. Map them to content.
- Traffic-source splits become usable (if one source has enough views).
- Compare CTR and retention across the creator's videos to find what differs.

### High (10,000+)
- Every noticeable dip/spike is meaningful.
- **Segment**: traffic source, new vs returning, device (mobile vs TV vs desktop), country
  /language, subscribed vs not.
- **Time slices**: early (first 48h, fan-heavy) vs later (colder audience). Retention and
  CTR usually drop as reach broadens — this is expected. A big drop only in later viewers
  means the video works for fans but not for strangers (packaging/hook assumes context).
- **Audience broadening**: identify when/where the video broke out (e.g., Browse or
  Suggested jumped) and what the new audience's retention looks like.
- **Winner analysis**: identify what's replicable — topic, angle, title structure, thumbnail
  composition, hook type, length, pacing, format — and what was luck/timing (trend, news,
  a big channel linking it).
- **Ceiling analysis**: even winners leave value on the table. Find the biggest dips and
  the longest outro — those are the next video's upside.

## Diagnosing "why so few views?" (the low-view decision tree)

```
Low views
├── Impressions very low?
│   ├── Yes → distribution problem
│   │   ├── New/small channel: platform lacks data about who to show it to →
│   │   │   consistent topic, clear packaging, post regularly, collaborations
│   │   ├── Topic has little demand → check search/trend interest, competitor results
│   │   └── Early viewers (subs) didn't respond → packaging/hook for the core audience
│   └── No → continue
├── CTR / viewed-vs-swiped low (vs creator's baseline)?
│   └── Yes → packaging problem (title, thumbnail, first frame, topic appeal)
├── Early retention low (hook zone)?
│   └── Yes → hook problem or promise mismatch
├── Middle slope steep / cliffs?
│   └── Yes → body problem (pacing, structure, open loops)
├── Retention OK but engagement/subs very low?
│   └── Yes → satisfaction problem (payoff weak, no reason to care, no CTA at the peak)
└── Everything decent but still small?
    └── Patience + volume: small channels grow in steps; the next video's packaging and
        topic choice matter more than micro-edits here.
```

## Diagnosing "why did this one blow up?" (high-view)

Check in order:
1. **Packaging**: what's different about this title/thumbnail vs the creator's others?
2. **Topic**: broader appeal? Trend? Search demand? A universal emotion?
3. **Hook**: faster to the point? Stronger promise? Visual confirmation earlier?
4. **Structure**: more open loops? Better escalation? Stronger ending?
5. **Traffic source**: where did the surge come from (Browse, Suggested next to a big video,
   Shorts feed, external share)? That tells you who the new audience is.
6. **Timing/luck**: news, trend, collaboration, a share from a large account.

Output: a "repeat this" list and a "this was luck" list. Be honest about which is which.

## Comparing videos fairly

- Compare at the same age (e.g., first 7 days) — not a 2-year-old video vs a 2-day-old one.
- Compare similar lengths and formats (don't compare a Short's APV to a 20-min video's).
- Normalize: views ÷ subscribers, subs gained ÷ 1,000 views, engagement ÷ views.
- Look for patterns across ≥3–5 videos before calling something a rule.
