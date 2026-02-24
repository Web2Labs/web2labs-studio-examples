# 10 - Webhook Automation

Fire-and-forget video processing. Upload a video with a webhook URL, and Studio sends a signed callback to your server when rendering finishes. No polling required.

## When to Use

- You're building an automated pipeline (upload video, get results via callback)
- You want to process videos without keeping a session open
- You're integrating Studio into a larger system (CMS, publishing pipeline, Discord bot)

## What You Get

- Video uploaded and processing starts immediately
- Your webhook receives a `project.completed` callback when done
- Callback includes project ID, output URLs, and metadata
- HMAC-SHA256 signature for verification

## Conversation

```
You:    Upload ~/Desktop/episode.mp4 as youtube and send results to
        https://my-server.com/studio/callback

Agent:  Checking credits... You have 8 API credits remaining.

        Uploading with 'youtube' preset + webhook...
        ├── Webhook URL:    https://my-server.com/studio/callback
        └── Upload complete. Project ID: p_w1x2y3

        Processing has started. You'll receive a signed callback at
        https://my-server.com/studio/callback when rendering finishes.

        No need to keep this session open — Studio will POST to your
        webhook when done. You can still check status anytime with
        "What's the status of project p_w1x2y3?"
```

## With Webhook Secret (Signed Callbacks)

For production use, add a secret so you can verify callbacks are genuinely from Studio:

```
You:    Upload ~/Desktop/episode.mp4 as youtube with webhook
        https://my-server.com/callback and secret "my-webhook-secret-123"

Agent:  Uploading with webhook + HMAC signing...
        ├── Webhook URL:    https://my-server.com/callback
        ├── Signing:        HMAC-SHA256 with your secret
        └── Upload complete. Project ID: p_s1t2u3

        Callbacks will include:
        ├── X-Web2Labs-Webhook-Timestamp (unix timestamp)
        └── X-Web2Labs-Webhook-Signature (sha256=<hmac>)

        Verify with: hmac_sha256(secret, timestamp + "." + body)
```

## Callback Payload

Your webhook receives a POST with this structure:

```json
{
  "event": "project.completed",
  "project_id": "p_w1x2y3",
  "status": "completed",
  "outputs": {
    "main": "https://...",
    "shorts": ["https://...", "..."],
    "subtitles": "https://...",
    "transcription": "https://..."
  },
  "metadata": {
    "title": "...",
    "description": "...",
    "duration_original": 2702,
    "duration_edited": 2185,
    "shorts_count": 27
  }
}
```

## Use Cases

| Pipeline | How It Works |
|----------|-------------|
| **Auto-publish** | Webhook triggers YouTube upload via YouTube API |
| **Discord bot** | Webhook posts download links to a Discord channel |
| **CMS integration** | Webhook creates a new post with embedded video |
| **Batch pipeline** | Upload 50 videos with webhooks, collect results asynchronously |
| **Client delivery** | Webhook sends email to client with download links |

## Cost

1 API credit per video. Webhooks are free — they're just a notification mechanism.
