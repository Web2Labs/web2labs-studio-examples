# 06 - Batch Processing

Process multiple videos in one go. The agent finds all matching files, confirms the total credit cost, and processes them sequentially.

## When to Use

- You have a folder of recordings that all need editing
- You're an agency processing client videos
- You recorded multiple segments and want them all cleaned up

## What You Get

- Each video processed independently with its own output folder
- Credit cost confirmation before any processing starts
- Sequential processing with progress updates per video

## Conversation

```
You:    Process all videos in ~/recordings/ as youtube videos

Agent:  Checking credits... You have 15 API credits remaining.

        Found 5 video files in ~/recordings/:
        ├── episode-43.mp4    (32:14, 1.2GB)
        ├── episode-44.mp4    (28:07, 980MB)
        ├── episode-45.mp4    (41:22, 1.5GB)
        ├── interview-jan.mp4 (55:18, 2.1GB)
        └── tutorial-react.mp4 (22:45, 890MB)

        This will process 5 videos and consume 5 API credits.
        You'll have 10 remaining after. Proceed?

You:    Yes, go ahead

Agent:  Processing 5 videos with 'youtube' preset...

        [1/5] episode-43.mp4
        ├── Uploading... done
        ├── Processing... 142 cuts, 27 shorts
        └── Complete (5m 12s)

        [2/5] episode-44.mp4
        ├── Uploading... done
        ├── Processing... 118 cuts, 24 shorts
        └── Complete (4m 38s)

        [3/5] episode-45.mp4
        ├── Uploading... done
        ├── Processing... 198 cuts, 32 shorts
        └── Complete (7m 15s)

        [4/5] interview-jan.mp4
        ├── Uploading... done
        ├── Processing... 267 cuts, 35 shorts
        └── Complete (9m 44s)

        [5/5] tutorial-react.mp4
        ├── Uploading... done
        ├── Processing... 94 cuts, 19 shorts
        └── Complete (3m 51s)

        All 5 videos complete. Total time: 30m 40s.
        Want me to download all results?

You:    Download everything

Agent:  Downloaded to ~/studio-exports/:
        ├── episode-43/      (main.mp4, shorts/, subtitles, transcription)
        ├── episode-44/      (main.mp4, shorts/, subtitles, transcription)
        ├── episode-45/      (main.mp4, shorts/, subtitles, transcription)
        ├── interview-jan/   (main.mp4, shorts/, subtitles, transcription)
        └── tutorial-react/  (main.mp4, shorts/, subtitles, transcription)

        10 API credits remaining.
```

## Cost Confirmation

The agent always confirms total cost before batch processing. This is enforced regardless of spend policy — batch jobs always get explicit confirmation.

## Tips

- **Mix presets per file:** "Process episode-43.mp4 as youtube and interview-jan.mp4 as podcast"
- **Estimate first:** "How much would it cost to process all videos in ~/recordings/?"
- **Partial batch:** "Process the latest 3 videos in ~/recordings/ as youtube"

## Cost

1 API credit per video. N videos = N credits.
