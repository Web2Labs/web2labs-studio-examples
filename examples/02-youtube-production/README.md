# 02 - YouTube Production

The full YouTube workflow: edited video, 25+ shorts, subtitles, transcription, and optionally thumbnails and brand-matched output. This is the workflow most creators will use daily.

## When to Use

- You recorded a YouTube video and want it publish-ready
- You want shorts auto-extracted for YouTube Shorts, TikTok, Instagram Reels
- You want subtitles baked in or as a separate .srt file

## What You Get

- Edited main video with jump-cuts, dynamic zoom punch-ins, and animated captions
- 25+ vertical shorts auto-extracted from your best moments
- Subtitles (.srt) and full transcription (.json)
- AI-generated metadata (title, description, tags, chapters, pinned comment)

## Conversation

```
You:    Edit ~/Desktop/episode-47.mp4 as a youtube video

Agent:  Checking credits... You have 8 API credits remaining.

        Uploading ~/Desktop/episode-47.mp4 with 'youtube' preset...
        Upload complete. Project ID: p_x7y8z9

        Waiting for processing...
        ├── Transcribing... (chunk 1/5)
        ├── Transcribing... (chunk 2/5)
        ├── Transcribing... (chunk 3/5)
        ├── Transcribing... (chunk 4/5)
        ├── Transcribing... (chunk 5/5)
        ├── Editing... 142 cuts, 38 zoom punch-ins
        ├── Generating shorts... 27 clips identified
        ├── Rendering main video... 60%
        ├── Rendering main video... 100%
        ├── Rendering shorts... 12/27
        ├── Rendering shorts... 27/27
        └── Complete! (7m 48s)

        Results:
        ├── main.mp4            45:02 → 36:18 (19% tighter)
        ├── shorts/             27 vertical clips (0:22 - 0:59 each)
        ├── subtitles.srt       891 entries
        ├── transcription.json  8,240 words
        └── metadata
            ├── title:          "Building a REST API from Scratch"
            ├── description:    (SEO-optimized, 280 words)
            ├── tags:           rest, api, tutorial, nodejs, ...
            ├── chapters:       12 auto-generated chapters
            └── pinned comment: (engagement hook + timestamps)

        Want me to download everything?
        Tip: I can also generate A/B/C thumbnail variants (10 Creator Credits).

You:    Yes, download everything. Skip thumbnails for now.

Agent:  Downloaded to ~/studio-exports/episode-47/:
        ├── main.mp4
        ├── shorts/
        │   ├── short-01.mp4 through short-27.mp4
        │   └── metadata.json (titles + descriptions per short)
        ├── subtitles.srt
        ├── transcription.json
        └── metadata.json

        7 API credits remaining.
```

## With Brand Import (First Time)

If this is your first time, import your brand so thumbnails and subtitles match your channel:

```
You:    Import my brand from https://youtube.com/@mychannel, then edit
        ~/Desktop/episode-47.mp4 as a youtube video

Agent:  Importing brand from YouTube...
        ├── Primary color: #1a73e8
        ├── Secondary color: #ff6f00
        ├── Channel name: "My Channel"
        ├── Identity: "Tech educator focused on practical web dev tutorials"
        └── Applied to your brand kit.

        Now uploading ~/Desktop/episode-47.mp4 with 'youtube' preset...
        (subtitles and future thumbnails will use your brand colors)
```

## Preset Used

`youtube` — Full production package. Subtitles + shorts + metadata. Dynamic zoom enabled. Audio normalization to broadcast standard (-14 LUFS).

## Cost

1 API credit for processing. Thumbnails are an optional add-on (10 Creator Credits).
