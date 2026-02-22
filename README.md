# Web2Labs Studio x OpenClaw - Examples

Copy-ready prompt workflows for the Web2Labs Studio OpenClaw skill.

## Quick Start

1. `clawhub install @web2labs/studio`
2. `Set up Web2Labs with my email you@example.com`
3. `Edit ~/Desktop/my-video.mp4 as a youtube video`

## Examples

- [01 Basic Edit](examples/01-basic-edit/)
- [02 YouTube Production](examples/02-youtube-production/)
- [03 Shorts from URL](examples/03-shorts-from-url/)
- [04 Gaming Montage](examples/04-gaming-montage/)
- [05 Podcast Cleanup](examples/05-podcast-cleanup/)
- [06 Batch Processing](examples/06-batch-processing/)
- [07 Twitch Automation](examples/07-twitch-automation/)
- [08 Custom Configuration](examples/08-custom-configuration/)

## Rush Processing Tip

When the user is time-constrained, include `priority: "rush"` on upload.
Rush processing costs 2 API credits instead of 1 and should be confirmed before running.
If spend policy requires confirmation, run the upload with `confirm_spend: true` after user approval.

## Brand Consistency Tip

Use `studio_brand` to set colors/identity once, then future thumbnails/subtitles inherit brand defaults.

## Reusable Media Tip

Use `studio_assets` to upload reusable `intro`, `outro`, and `watermark` assets, then enable defaults with `studio_brand` for future projects.

## Automation Tip (Webhooks)

For fire-and-forget flows, pass `webhook_url` (and optional `webhook_secret`) on `studio_upload` and continue when your callback receives `project.completed`.

## Links

- https://clawhub.com/@web2labs/studio
- https://web2labs.com/openclaw
- https://web2labs.com/docs-api
