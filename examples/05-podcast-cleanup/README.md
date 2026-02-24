# 05 - Podcast Cleanup

Clean up podcast and interview recordings with gentle, conversation-aware cuts. Removes long pauses and dead air while preserving the natural flow of dialogue.

## When to Use

- You recorded a podcast episode or interview
- You want dead air removed but the conversational flow preserved
- You need clean subtitles for accessibility
- You don't want aggressive cuts or zoom effects

## What You Get

- Edited video with soft jump-cuts (silence and dead air removed, natural pacing kept)
- No zoom punch-ins (preserves the talking-head/interview feel)
- Subtitles (.srt) optimized for spoken conversation
- Full transcription

## Conversation

```
You:    Clean up ~/Podcasts/ep-42-interview.mp4 with the podcast preset

Agent:  Checking credits... You have 6 API credits remaining.

        Uploading with 'podcast' preset...
        Upload complete. Project ID: p_p1q2r3

        Waiting for processing...
        ├── Transcribing... (chunk 1/12)
        ├── ...
        ├── Transcribing... (chunk 12/12)
        ├── Editing... 87 soft cuts applied
        ├── Rendering...
        └── Complete! (11m 33s)

        Results:
        ├── main.mp4            1:24:10 → 1:12:45 (14% tighter)
        ├── subtitles.srt       1,842 entries
        └── transcription.json  16,480 words

        The podcast preset kept cuts gentle — no zoom, no music overlay.
        Want me to download?

You:    Yes please

Agent:  Downloaded to ~/studio-exports/ep-42-interview/
        5 API credits remaining.
```

## What Makes Podcast Different

The `podcast` preset adjusts AI behavior:
- **Soft cuts only** — longer silence threshold before cutting (preserves natural pauses in conversation)
- **No zoom** — talking-head and interview formats look wrong with random zoom punch-ins
- **No music overlay** — podcasts have their own audio character
- **Conversation-aware** — AI understands turn-taking and preserves speaker transitions
- **Subtitle focus** — high-quality subtitles since podcast audiences value accessibility

## Preset Used

`podcast` — Soft cuts, subtitles, no zoom, no music. Built for talking-head and interview formats.

## Cost

1 API credit.
