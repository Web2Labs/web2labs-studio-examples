# FAQ

## Getting Started

### Do I need a subscription?

No. You get 2 free API credits when you generate your first API key. Each credit processes one video. After that, you can buy credit bundles starting at €22.99 for 10 credits, or subscribe for lower per-video costs.

### How do I sign up?

Tell your AI assistant: "Set up Web2Labs with my email you@example.com". A magic link is sent to your email. Click the link or enter the code, and your API key is generated automatically.

### Can I use an existing API key?

Yes. If you already have an API key from web2labs.com, tell your agent: "Save my Web2Labs API key sk_live_xxxxx". It's stored locally in `~/.openclaw/openclaw.json`.

### What AI assistants work with this skill?

Any AI assistant that supports OpenClaw skills or MCP (Model Context Protocol) tools. This includes Claude, ChatGPT, Cursor, and others with MCP support.

## Videos & Processing

### What video formats are supported?

MP4, MOV, MKV, AVI, WebM, and most common video formats. MP4 is recommended.

### How long can my video be?

There's no hard limit, but processing time scales with video length. A 10-minute video takes ~3-5 minutes to process; a 2-hour video can take 30-60 minutes.

### Can I use YouTube or Twitch URLs instead of local files?

Yes, with `yt-dlp` installed locally. The video is downloaded to your machine first, then uploaded to Studio. Install with `brew install yt-dlp` (macOS), `pip install yt-dlp` (Linux), or `winget install yt-dlp` (Windows).

### Where are my files downloaded?

Default: `~/studio-exports/<project-name>/`. You can specify a custom path in your prompt.

### How long are processed files kept?

Depends on your plan. Free users: 2 hours. Paid users: varies by tier (check your plan details). Always download outputs promptly.

### Can I re-edit without re-uploading?

Yes. Use "Re-render my last project with [changes]". The first re-render per project is free; subsequent re-renders cost 15 Creator Credits.

## Credits & Pricing

### How much does it cost?

1 API credit per video. Your first 2 are free. Bundles: 10 for €22.99, 20 for €39.99, 100 for €199.99. Subscribers get monthly credits at lower per-video cost.

### What are Creator Credits?

A separate currency for premium features like thumbnail generation (10 CC), re-renders (15 CC after the first free one), and future premium add-ons. They're different from API credits.

### How do I check my balance?

Tell your agent: "How many credits do I have?" or "Check my credits."

### Can I estimate costs before processing?

Yes. Tell your agent: "How much would it cost to process this video?" before uploading. Especially useful for batch jobs.

### What's rush priority?

Rush processing costs 2 API credits instead of 1 and moves your job to the front of the render queue. The agent always confirms before spending extra.

## Referrals

### How do referrals work?

Every user gets a unique referral code (format: STUDIO-XXXX). When someone signs up with your code, you both get 5 free API credits (60-day expiry). Ask your agent: "What's my referral code?"

### How many referrals can I make?

Up to 10 referrals (50 free credits total). Referred users must apply the code within 24 hours of creating their account.

## Brand & Assets

### What is the brand kit?

Your brand kit stores your channel name, colors, identity description, and font preferences. Once set, thumbnails and subtitles automatically use your brand style.

### Can I import my brand from YouTube?

Yes. Tell your agent: "Import my brand from https://youtube.com/@mychannel". It auto-detects your colors and channel identity.

### What assets can I upload?

Intros (video), outros (video), and watermarks (image). Once uploaded, they're applied to future renders automatically.

## Watch Mode

### What is watch mode?

Watch mode monitors a YouTube or Twitch channel for new uploads and auto-processes them through Studio. Stream on Twitch, and edited YouTube-ready videos appear without manual intervention.

### Does it run automatically?

The watcher stores configuration locally. You need to trigger checks — either by telling your agent "Check my watchers" or setting up a cron job. It doesn't run in the background continuously.

### Can I watch someone else's channel?

Only watch channels you own or have explicit permission to process.
