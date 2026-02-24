# 01 - Basic Edit

The fastest path from raw recording to cleaned-up video. One prompt, one credit, done.

## When to Use

- You have a local recording and want dead air, filler, and silences removed
- You don't need shorts, thumbnails, or any extras — just a clean edit
- You want to test Studio for the first time

## What You Get

- Edited video with jump-cuts, tighter pacing, and normalized audio
- Subtitles file (.srt)
- Full transcription (.json)

## Conversation

```
You:    Edit ~/Desktop/my-recording.mp4

Agent:  Checking credits... You have 2 API credits remaining.

        Uploading ~/Desktop/my-recording.mp4 with 'quick' preset...
        Upload complete. Project ID: p_a1b2c3d4

        Waiting for processing...
        ├── Transcribing... (chunk 1/3)
        ├── Transcribing... (chunk 2/3)
        ├── Transcribing... (chunk 3/3)
        ├── Editing... smart cuts applied
        ├── Rendering... 45%
        ├── Rendering... 90%
        └── Complete! (4m 12s)

        Results:
        ├── main.mp4       22:14 → 18:41 (16% tighter)
        ├── subtitles.srt   412 subtitle entries
        └── transcription   3,847 words

        Want me to download these files?

You:    Yes, download everything

Agent:  Downloaded to ~/studio-exports/my-recording/:
        ├── main.mp4              (18:41, 847MB)
        ├── subtitles.srt
        └── transcription.json

        You have 1 API credit remaining.
        Tip: Want shorts and thumbnails next time? Try the 'youtube' preset.
```

## Preset Used

`quick` — Fast cleanup, no extras. Removes dead air, normalizes audio, generates subtitles. No shorts, no music, no thumbnails.

## Cost

1 API credit per video. Your first 2 videos are free.
