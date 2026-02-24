# Common Errors

## Authentication

### `missing_auth`
**Cause:** No API key configured.
**Fix:** Run `studio_setup` or tell your agent "Set up Web2Labs with my email". If you have an existing key, say "Save my Web2Labs API key sk_live_xxxxx".

### `invalid_api_key`
**Cause:** API key is malformed or revoked.
**Fix:** Generate a new key at web2labs.com/user/api, or run `studio_setup` again.

### `unauthorized`
**Cause:** API key doesn't have access to the requested resource.
**Fix:** Verify you're using the correct key and that your account is active.

## Credits

### `no_api_credit`
**Cause:** API credit balance is zero.
**Fix:** Purchase credits at web2labs.com/pricing or use subscription bearer auth. Check balance with "How many credits do I have?"

### `monthly_limit_reached`
**Cause:** Subscription monthly project limit exhausted.
**Fix:** Wait for the next billing cycle, purchase API credit bundles for additional capacity, or upgrade your tier.

### `insufficient_creator_credits`
**Cause:** Not enough Creator Credits for a premium feature (thumbnails, re-render).
**Fix:** Purchase Creator Credit bundles. Ask your agent "Show me pricing" for options.

## Processing

### `worker_unavailable`
**Cause:** No render worker is currently online.
**Fix:** Retry in a few minutes. If persistent, check status at web2labs.com or contact support.

### `processing_failed`
**Cause:** Video processing failed during transcription, cutting, or rendering.
**Fix:** Note the project ID and report via "Submit feedback about project p_xxxxx". Common causes: corrupted video file, unsupported codec, or very short video with no speech.

### `no_spoken_audio`
**Cause:** Studio couldn't detect spoken audio in the recording.
**Fix:** Studio needs speech to generate jump-cuts and subtitles. Ensure your recording has narration or conversation. Background music alone is not enough.

### `upload_too_large`
**Cause:** File exceeds the upload size limit.
**Fix:** Check your tier's file size limit. Consider compressing the video or splitting it into shorter segments.

## URL Downloads

### `yt-dlp is not installed`
**Cause:** URL-based workflows require yt-dlp, which isn't found on your system.
**Fix:** Install it:
- macOS: `brew install yt-dlp`
- Linux: `pip install yt-dlp`
- Windows: `winget install yt-dlp`

### `yt-dlp download failed`
**Cause:** The URL is private, geo-restricted, or the platform blocked the download.
**Fix:** Verify the URL is accessible. For private videos, download manually and use the local file path instead.

### `unsupported_url`
**Cause:** The URL doesn't match a supported platform (YouTube, Twitch, Vimeo).
**Fix:** Download the video manually and upload the local file instead.

## Rate Limiting

### `429 Too Many Requests`
**Cause:** You've exceeded the API rate limit.
**Fix:** The agent automatically retries with backoff. If persistent, wait a minute before trying again. Status polling has a tighter limit (10 requests per 10 seconds).

## Network

### `ECONNREFUSED` / `ETIMEDOUT`
**Cause:** Can't reach the Studio API server.
**Fix:** Check your internet connection. If you're behind a corporate proxy, ensure HTTPS traffic to web2labs.com is allowed.

### `socket_connection_failed`
**Cause:** WebSocket connection for real-time progress failed.
**Fix:** The skill falls back to HTTP polling automatically. If you're behind a firewall that blocks WebSocket upgrades, the skill still works — progress updates just come via HTTP polling instead.

## Sandbox Mode

### API key not found in sandbox
**Cause:** Environment variables from the host aren't available inside the Docker sandbox.
**Fix:** After starting the session, tell your agent "Save my API key sk_live_xxxxx". This writes the key to a config file inside the container. See the SKILL.md sandbox section for details.
