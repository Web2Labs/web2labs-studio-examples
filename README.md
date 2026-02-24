# Web2Labs Studio - OpenClaw Examples

Copy-paste prompt workflows for the `@web2labs/studio` skill.
Each example shows the exact prompts to use, what the agent does behind the scenes, and what you get back.

## Install

```bash
clawhub install @web2labs/studio
```

Then tell your AI assistant:

```
Set up Web2Labs with my email you@example.com
```

You get 2 free credits. No credit card required.

## Examples

| # | Workflow | Who It's For | Credits |
|---|----------|-------------|---------|
| [01](examples/01-basic-edit/) | **Basic Edit** | First-time users | 1 |
| [02](examples/02-youtube-production/) | **YouTube Production** | YouTubers who want the full package | 1 + optional CC |
| [03](examples/03-shorts-from-url/) | **Shorts from URL** | Social media managers, repurposers | 1 |
| [04](examples/04-gaming-montage/) | **Gaming Montage** | Streamers, gamers | 1 |
| [05](examples/05-podcast-cleanup/) | **Podcast Cleanup** | Podcasters, interviewers | 1 |
| [06](examples/06-batch-processing/) | **Batch Processing** | Agencies, multi-video creators | N |
| [07](examples/07-twitch-automation/) | **Twitch Automation** | Twitch streamers who want hands-off YouTube | 1/VOD |
| [08](examples/08-custom-configuration/) | **Custom Configuration** | Power users who want full control | 1 |
| [09](examples/09-brand-and-thumbnails/) | **Brand Kit + Thumbnails** | Creators building a consistent brand | CC |
| [10](examples/10-webhook-automation/) | **Webhook Automation** | Developers, pipeline builders | 1 |

**CC** = Creator Credits (separate from API credits; used for premium features like thumbnails)

## How to Read These Examples

Each example contains:

- **README.md** — What the workflow does, when to use it, and a full conversation showing exactly what you say and what the agent responds with
- **prompts.md** — Standalone prompt variations you can copy-paste directly

The conversation examples show realistic multi-turn interactions. Your actual output will vary based on your video content.

## Tips

**Check credits first.** Say "How many credits do I have?" before starting. The agent calls `studio_credits` and tells you your balance.

**Use presets.** Instead of configuring everything manually, start with a preset (`youtube`, `quick`, `shorts-only`, `podcast`, `gaming`, `tutorial`, `vlog`, `cinematic`) and override what you need.

**Estimate before large jobs.** Say "How much will this cost?" before batch processing. The agent calls `studio_estimate` and confirms before spending.

**Set up your brand once.** Say "Import my brand from https://youtube.com/@mychannel" to auto-detect your colors and identity. Every future video inherits your brand.

**Earn free credits.** Say "What's my referral code?" to get your link. Each friend who signs up gives you both 5 free credits.

## Links

- [ClawHub Listing](https://clawhub.com/@web2labs/studio)
- [Landing Page](https://web2labs.com/openclaw)
- [API Docs](https://web2labs.com/api/v1/docs)
- [Pricing](https://web2labs.com/pricing)
