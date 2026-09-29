# Reading Retention Curves

A retention curve is a record of thousands of tiny decisions. Read it like a story: where
did people lean in, where did they give up, and what was on screen when they did.

## Anatomy of a curve

```
100% ┤█
     │ █▄                       ← initial drop (hook zone)
     │   ▀▄▄
     │      ▀▀▀▄▄▄▄             ← body: gentle slope = healthy
     │             ▀▄  ▄▀▄      ← dip = event; spike = rewind/rewatch
     │               ▀▀   ▀▄▄▄
     │                       ▀▄ ← outro drop (normal when content ends)
   0 ┼──────────────────────────
     0:00                    end
```

Zones:
1. **Hook zone** — long-form: 0:00–0:30 (most of the loss happens in the first 5–15s).
   Short-form: 0:00–0:03, then 0:03–0:10.
2. **Setup/transition** — where the video shifts from "promise" to "delivery". Common place
   for a second drop if the setup is long.
3. **Body** — the main value. Should decline slowly and steadily.
4. **Payoff** — the moment the promise is fulfilled.
5. **Outro** — post-payoff. Viewers leave once they feel "done". This drop is normal; a
   long outro makes it bigger and lowers AVD.

## Normal decay vs events

- **Normal decay**: smooth, slowly declining slope. Every video has it. People leave for
  reasons unrelated to content (phone call, bus stop). Don't over-diagnose it.
- **Events**: a slope that suddenly steepens (**dip / cliff**), goes flat (**plateau**), or
  rises (**spike**). Events are where analysis pays off.

Rule of thumb: an event is worth investigating if it's clearly steeper than the surrounding
slope *and* the data regime supports it (see `low-vs-high-view.md`).

## Curve shapes and what they usually mean

| Shape | What it looks like | Usual meaning | First things to check |
|---|---|---|---|
| **Cliff then flat** | Big early drop, then very stable | Hook/packaging mismatch — those who stay love it, many arrivals didn't get what they expected | Does the first 5s visibly confirm the title/thumbnail promise? |
| **Healthy slope** | Moderate early drop, gentle steady decline | Working video | Look for small wins: shorten outro, tighten setup |
| **Steady slide** | No big cliffs, constant steep decline | Pacing/density problem throughout; no reason to keep watching | Open loops? Visual change rate? Rambling? |
| **Staircase** | Plateaus separated by drops | Drops at section transitions — each section "ends" and gives a natural exit | Bridge sections with forward hooks; remove "that's it for X" language |
| **Early cliff at payoff** | Big drop mid-video | Payoff/answer given too early; viewers got what they came for | Move reveal later or add a second, bigger reason to stay |
| **Late cliff** | Stable until a sudden late drop | A specific moment: sponsor read, "before we wrap up", recap, CTA, tone shift | What exactly starts at that timestamp? |
| **Sawtooth** | Repeated small dips and bumps | Viewers skipping/scrubbing — hunting for the good parts | Content is valued but padded; chapters/tighter edit |
| **Rising end / >100%** | Curve lifts at end (common in shorts) | Loops/rewatches — the ending returns to the start or begs rewatching | Great sign; make the loop intentional |
| **Spike mid-video** | Local bump | Rewind to rewatch: something impressive, confusing, or funny | Is it confusion (fix: clarify) or delight (fix: do more of it)? |
| **Flat line high** | Very high retention throughout, low views | Great content, weak packaging/distribution | Title, thumbnail, topic demand |

## Diagnosing a dip: the 5-question method

For each meaningful dip at timestamp T:
1. **What was on screen/said at T and 2–10s before T?** (People decide before they leave.)
2. **Did the video just satisfy or disappoint a question?** Answer given → "done". Answer
   delayed with no progress → "not worth waiting".
3. **Did the energy/format change?** (Talking head after B-roll, music drops, sponsor, slide.)
4. **Did it get confusing or repetitive?** (Jargon, re-explaining, saying the same thing twice.)
5. **Did it signal an ending?** ("So, in conclusion", "that's basically it", "lastly".)

Write the answer as: `T → content → viewer feeling → cause → fix`.

## Diagnosing a spike

- **Delight spike**: striking visual, joke, reveal, satisfying moment → do more of this,
  and consider moving a version of it earlier (hook) or into the thumbnail.
- **Confusion spike**: fast explanation, small text, unclear visual → viewers rewind to
  understand; slow down, add on-screen text, simplify.
- **Skip-target spike**: people jumping ahead land here — often the moment the thumbnail
  showed. That means the stuff before it is felt as a delay. Move it earlier or tease it.
- **Chapter/seek spike**: a chapter start. Tells you which topic viewers wanted most.

## Hook-zone benchmarks (heuristics, not laws)

These vary heavily by niche, length, and traffic source; use the creator's own history as
the real benchmark whenever possible.
- Long-form: holding roughly 65–75%+ at 0:30 is generally strong; below ~50% points at a
  hook or packaging problem.
- Shorts/TikTok/Reels: the fight is the first 1–3 seconds. A high swipe-away/skip rate means
  the first frame and first line aren't earning attention.
- Overall long-form APV: compare to the creator's own videos of similar length and the
  relative-retention graph, not to a universal number.

Always phrase benchmarks as "typically" — never as guaranteed thresholds.

## Mapping curve → content

To connect the graph to content precisely:
1. Get a timestamped transcript (YouTube auto-captions, or the editing project).
2. List every event with its timestamp.
3. For each, quote the transcript lines at T−10s to T and describe the visuals.
4. Cross-check against the simulated-viewer pass (`human-attention.md`).
5. Only then write fixes.

If you only have a screenshot of the graph, estimate timestamps from the axis and say
they're approximate (±2–5% of video length).
