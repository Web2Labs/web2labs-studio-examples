# 08 - Custom Configuration

Start with a preset and override specific settings. Full control without configuring everything from scratch.

## When to Use

- You like a preset but want to tweak one or two things
- You want a specific number of shorts, or a specific subtitle style
- You want to disable music, change zoom behavior, or adjust cut sensitivity

## What You Get

The same output as the base preset, but with your overrides applied.

## Conversation

```
You:    Edit ~/Desktop/episode.mp4 as youtube but with 5 shorts, no music,
        and large subtitles

Agent:  Checking credits... You have 9 API credits remaining.

        Uploading with 'youtube' preset + overrides:
        ├── Music: disabled
        ├── Shorts: max 5
        └── Subtitles: large font with highlight

        Upload complete. Project ID: p_c1d2e3

        Waiting for processing...
        ├── Transcribing...
        ├── Editing... 156 cuts, 42 zoom punch-ins
        ├── Generating shorts... 5 clips (capped at your limit)
        ├── Rendering...
        └── Complete! (6m 08s)

        Results:
        ├── main.mp4          38:22 → 31:05 (19% tighter)
        ├── shorts/           5 vertical clips
        ├── subtitles.srt     (large font, highlight enabled)
        └── transcription.json

        Want me to download?
```

## Common Overrides

| What You Say | What It Does |
|-------------|-------------|
| "no music" | Disables background music overlay |
| "no shorts" | Skips short-form clip generation |
| "5 shorts" | Caps shorts at 5 instead of auto |
| "no zoom" | Disables dynamic zoom punch-ins |
| "large subtitles" | Uses larger subtitle font preset |
| "minimal subtitles" | Clean, unobtrusive subtitle style |
| "no subtitles" | Disables subtitle rendering entirely |
| "gentle cuts" | Less aggressive cutting (more like podcast) |
| "aggressive cuts" | More aggressive cutting (more like gaming) |

## Configuration JSON Reference

For programmatic use, here's what the overrides look like under the hood:

```json
{
  "preset": "youtube",
  "configuration": {
    "musicEnabled": false,
    "shortsConfig": {
      "amount": 5,
      "minLength": 20,
      "maxLength": 60
    },
    "subtitleConfig": {
      "fontSizePreset": "large",
      "enableHighlight": true
    },
    "zoomConfig": {
      "enabled": false
    }
  }
}
```

You don't need to write JSON — just describe what you want in natural language and the agent translates it.

## Cost

1 API credit. Overrides don't change the cost.
