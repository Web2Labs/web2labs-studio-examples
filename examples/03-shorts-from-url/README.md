# 03 - Shorts from URL

Turn any YouTube or Twitch video into vertical shorts. Paste a URL, get back 25+ clips ready for TikTok, Instagram Reels, and YouTube Shorts.

Requires `yt-dlp` installed locally (`brew install yt-dlp` / `pip install yt-dlp` / `winget install yt-dlp`).

## When to Use

- You want to repurpose an existing YouTube video into short-form content
- You're a social media manager who needs clips from client videos
- You want shorts without the full edit — just the vertical clips

## What You Get

- 25+ vertical shorts (9:16, optimized for mobile)
- Each short has its own title and description
- Metadata file with hook timestamps and clip descriptions

## Conversation

```
You:    Make shorts from https://youtube.com/watch?v=dQw4w9WgXcQ

Agent:  Checking credits... You have 5 API credits remaining.

        Downloading video via yt-dlp...
        Downloaded: "Never Gonna Give You Up" (3:33, 48MB)

        Uploading with 'shorts-only' preset...
        Upload complete. Project ID: p_m4n5o6

        Waiting for processing...
        ├── Transcribing...
        ├── Editing... identifying best moments
        ├── Generating shorts... 8 clips identified
        ├── Rendering shorts... 8/8
        └── Complete! (2m 04s)

        Results:
        └── shorts/             8 vertical clips
            ├── short-01.mp4    (0:34) "The Ultimate Rickroll Origin"
            ├── short-02.mp4    (0:28) "Never Gonna Let You Down"
            ├── ...
            └── short-08.mp4    (0:41) "80s Dance Moves Compilation"

        Want me to download these?

You:    Download to ~/Shorts/rickroll/

Agent:  Downloaded 8 shorts to ~/Shorts/rickroll/
        4 API credits remaining.
```

## Supported URLs

| Platform | URL Format | Notes |
|----------|-----------|-------|
| YouTube | `youtube.com/watch?v=...` | Public and unlisted videos |
| YouTube | `youtu.be/...` | Short links work too |
| Twitch | `twitch.tv/videos/...` | VODs and clips |
| Vimeo | `vimeo.com/...` | Public videos |

Only process content you own or have permission to edit.

## Preset Used

`shorts-only` — Generates only vertical shorts. No main video edit, no subtitles file.

## Cost

1 API credit. The video is downloaded locally via yt-dlp before uploading to Studio.
