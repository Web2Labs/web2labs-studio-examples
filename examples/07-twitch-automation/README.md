# 07 - Twitch Automation

Set up a watcher on your Twitch (or YouTube) channel. Studio automatically downloads and processes new VODs, so you go live on Twitch and content appears on YouTube without touching an editor.

Requires `yt-dlp` installed locally.

## When to Use

- You stream on Twitch and want every VOD auto-edited for YouTube
- You want a "set and forget" content pipeline
- You want to repurpose stream highlights into shorts automatically

## What You Get

- Automatic detection of new VODs on your channel
- Each new VOD downloaded, uploaded to Studio, and processed with your chosen preset
- Configurable limits: max duration, max daily uploads, polling interval
- Processed video IDs tracked so nothing gets processed twice

## Conversation

### Setting Up

```
You:    Watch my Twitch channel https://twitch.tv/my_channel for new VODs

Agent:  Setting up watcher for 'my_channel'...

        Watcher created:
        ├── Channel:     https://twitch.tv/my_channel
        ├── Preset:      gaming
        ├── Max duration: 120 minutes (skips longer VODs)
        ├── Max daily:   5 uploads/day
        ├── Poll interval: 30 minutes
        └── Status:      enabled

        To check for new VODs, say "Check my watchers."
        For fully automatic processing, set up a cron job (see below).
```

### Checking for New Content

```
You:    Check my watchers

Agent:  Checking 1 watcher...

        my_channel: 2 new VODs found
        ├── "Ranked Grind Day 14" (1:42:18)
        │   └── Downloading... uploading... Project p_t1u2v3 created
        ├── "Late Night Chill Stream" (3:15:44)
        │   └── Skipped: exceeds 120 minute limit
        └── 1 video uploaded and processing

        Use "Check the status of project p_t1u2v3" to track progress.
```

### Listing Watchers

```
You:    Show my watchers

Agent:  You have 1 watcher:

        ┌─────────────────────────────────────────────────┐
        │ #1 — my_channel                                 │
        ├─────────────────────────────────────────────────┤
        │ Channel:   https://twitch.tv/my_channel         │
        │ Preset:    gaming                               │
        │ Status:    enabled                              │
        │ Processed: 4 videos total                       │
        │ Last check: 2 hours ago                         │
        └─────────────────────────────────────────────────┘
```

### Pausing / Removing

```
You:    Pause watcher #1

Agent:  Watcher #1 (my_channel) paused. No new VODs will be processed
        until you resume it.
```

## Scheduling Automatic Checks

The watcher stores configuration locally. To automate, have your agent check periodically or set up a system cron:

```bash
# Check every 30 minutes via cron
*/30 * * * * openclaw agent -m "Check my watchers" --skill @web2labs/studio
```

Or ask your agent to check on a schedule during a long session:

```
Check my watchers every 30 minutes and notify me when new videos are processed
```

## Supported Platforms

| Platform | Channel URL Format |
|----------|-------------------|
| Twitch | `https://twitch.tv/username` |
| YouTube | `https://youtube.com/@username` |

Individual video URLs are not accepted — use channel/user URLs only.

## Cost

1 API credit per VOD processed. Skipped videos (too long, already processed) cost nothing.
