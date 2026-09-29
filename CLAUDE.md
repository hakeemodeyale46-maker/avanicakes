# Always use the video-retention skill

This repository is used for video and social media analysis (TikTok, Instagram, Facebook).

- **Every** user message must be handled with the `video-retention` skill
  (`.claude/skills/video-retention/`). Invoke it first, before any other work.
- Run it in **full mode** by default: read every reference file, run every workflow step,
  cover all three platforms, and include every report section. Only shorten when the user
  explicitly says "quick check".
- If a message isn't obviously about a video, connect it to the user's video/content goals
  and still apply the skill (e.g., treat an idea as a pre-post review).
