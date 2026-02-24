# 09 - Brand Kit + Thumbnails

Set up your brand identity once, then every video you process inherits your colors, fonts, and style. Generate A/B/C thumbnail variants that match your brand.

## When to Use

- You want consistent branding across all your videos
- You want AI-generated thumbnails that match your channel's look
- You're setting up Studio for the first time and want to "teach it" your brand

## What You Get

- Brand kit saved to your account (colors, identity, fonts, channel name)
- Auto-import from your YouTube or Twitch channel
- Thumbnails styled to your brand (3 variants for A/B testing)
- Reusable intro/outro/watermark assets

## Conversation: Import Brand from YouTube

```
You:    Import my brand from https://youtube.com/@mychannel

Agent:  Analyzing your YouTube channel...

        Brand preview:
        ├── Channel name:   "My Channel"
        ├── Primary color:  #1a73e8
        ├── Secondary color: #ff6f00
        ├── Accent color:   #2196f3 (computed)
        ├── Identity:       "Tech educator creating practical web
        │                    development tutorials for beginners"
        └── Source:         youtube.com/@mychannel

        Apply these brand settings?

You:    Yes, apply it

Agent:  Brand kit updated. All future thumbnails and subtitles will use
        your brand colors. You can adjust anytime with "Update my brand."
```

## Conversation: Generate Thumbnails

```
You:    Generate thumbnails for my last project

Agent:  Generating A/B/C thumbnail variants for project p_x7y8z9...
        This costs 10 Creator Credits. You have 45 remaining. Proceeding.

        Thumbnails ready:
        ├── Variant A: Bold title + face close-up + brand gradient
        ├── Variant B: Minimal text + action shot + channel colors
        └── Variant C: Question hook + contrast background + logo

        Want me to download them?

You:    Download all three

Agent:  Downloaded to ~/studio-exports/episode-47/thumbnails/:
        ├── thumbnail-a.png
        ├── thumbnail-b.png
        └── thumbnail-c.png

        Tip: Upload all 3 to YouTube and let their A/B test pick the winner.
```

## Conversation: Upload Reusable Assets

```
You:    Upload ~/Videos/my-intro.mp4 as my intro

Agent:  Uploading intro asset...
        ├── File: my-intro.mp4 (4.2s, 12MB)
        └── Saved as default intro

        This intro will be prepended to all future renders that have
        intros enabled. Manage assets with "Show my assets."

You:    Also upload ~/Images/watermark.png as my watermark

Agent:  Uploading watermark asset...
        ├── File: watermark.png (128KB)
        └── Saved as default watermark

        Your assets:
        ├── Intro:     my-intro.mp4 (4.2s)
        ├── Outro:     (none)
        └── Watermark: watermark.png
```

## Conversation: Manual Brand Setup

If you don't have a YouTube channel to import from:

```
You:    Set my brand colors to primary #ff0000 and secondary #000000,
        channel name "RedZone Gaming"

Agent:  Brand kit updated:
        ├── Channel name:    RedZone Gaming
        ├── Primary color:   #ff0000
        ├── Secondary color: #000000
        └── Accent color:    #ff3333 (computed)

        These colors will be used for thumbnails and subtitle styling.
```

## Cost

- Brand import: free
- Brand update: free
- Asset upload: free
- Thumbnail generation: 10 Creator Credits per project
- Re-render with brand changes: first free, then 15 Creator Credits
