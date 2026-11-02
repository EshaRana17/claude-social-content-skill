# Social Content Studio (Agent Skill)

An open-source Agent Skill that turns Claude into a careful social media
content studio for creators, founders and small brands. It follows the open
[Agent Skills](https://agentskills.io/specification) `SKILL.md` format, so it
works in Claude Code, Claude.ai and other agents that support the standard.

Skill name: `social-content`

## What it does

| Workflow | Output |
|----------|--------|
| Repurpose one piece | From a blog post, video transcript or podcast notes: an X thread, LinkedIn post, Instagram carousel (slide-by-slide copy, alt text, caption), short-video script (hook, beats, on-screen text, CTA) and a Threads/Bluesky post |
| Hooks and headlines | Options across five named patterns (curiosity gap, contrarian, specific result, story open, list promise), why each works, and a payoff check against clickbait |
| Content calendar | A 30-day plan sized to your real capacity, with pillars, format mix, cadence, a weekly review loop and an import-ready CSV |
| Brand voice | A voice guide built from 3-5 of your posts (tone, vocabulary, rhythm, do/don't) and applied to new drafts |
| Post review | Scores for hook, clarity, scannability, CTA, platform fit, accessibility and honesty, plus an improved version |

Built-in guardrails: no fake engagement, no fake reviews or testimonials, no
posing as an unaffiliated customer, clear sponsorship and affiliation
disclosure (in line with US FTC endorsement guidance), no engagement bait and
no invented statistics. Missing facts are marked `[ADD: ...]` rather than
made up.

Platform limits (X, LinkedIn, Instagram, TikTok, YouTube Shorts, Threads,
Bluesky) are recorded with check dates in
[`references/platforms.md`](references/platforms.md). Limits change; update
that file when they do.

## Example prompts

- "Turn this blog post into an X thread, a LinkedIn post and an Instagram
  carousel." (paste the post)
- "Here is the transcript of my latest podcast episode. Give me a 45-second
  Reels script and a Bluesky post."
- "Write 10 hook options for a LinkedIn post about why we stopped offering
  free trials."
- "Build a 30-day content calendar for my bakery. Goal: more pre-orders.
  I have about 4 hours a week. Export it as CSV."
- "Here are five of my posts. Build me a voice guide, then rewrite this draft
  in my voice."
- "Review this LinkedIn draft and make it better."

## Repository layout

```
claude-social-content-skill/
  SKILL.md                    Main instructions (loaded when the skill triggers)
  references/
    platforms.md              Limits with dates, platform norms, disclosure tools
    hooks.md                  Hook patterns, strength and clickbait tests
    repurposing.md            Idea inventory, angle matrix, templates, example
    calendar.md               Pillars, cadence, CSV spec, review loop
    voice.md                  Voice analysis checklist and guide template
    ethics.md                 Disclosure, fake engagement, claims, examples
  assets/
    content_calendar.csv      Calendar template (header plus sample rows)
  agent.json                  Machine-readable manifest
  LICENSE                     MIT
  README.md
```

Reference files are loaded only when a workflow needs them (progressive
disclosure), keeping the main instructions short.

## Installation

The skill folder must be named `social-content` to match the `name` field in
`SKILL.md` (required by the Agent Skills specification). This repository is
named `claude-social-content-skill`, so rename the folder when you install it.

### Claude Code

Personal (available in all your projects):

```bash
git clone https://github.com/EshaRana17/claude-social-content-skill.git
mkdir -p ~/.claude/skills
cp -r claude-social-content-skill ~/.claude/skills/social-content
```

On Windows (PowerShell):

```powershell
git clone https://github.com/EshaRana17/claude-social-content-skill.git
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse claude-social-content-skill "$HOME\.claude\skills\social-content"
```

Project-only (shared with your team through the repo): copy the folder to
`.claude/skills/social-content/` in your project.

Claude Code loads the skill automatically when a request matches its
description. You can remove the `.git` folder from the installed copy.

### Claude.ai

1. Make sure code execution is enabled: Settings > Capabilities, turn on
   "Create and edit files" (Team and Enterprise owners enable skills in
   organization settings).
2. Rename the folder to `social-content` and zip it, so the ZIP contains the
   `social-content/` folder with `SKILL.md` inside.
3. Go to Customize > Skills, click "+", then "Create skill" and
   "Upload a skill".
4. Upload the ZIP and toggle the skill on.

Menu names can change; see Anthropic's help article "Using Skills in Claude"
if the steps differ.

### Other agents

Any agent that supports the Agent Skills `SKILL.md` standard can use this
folder as-is: place `social-content/` wherever that agent discovers skills.
The frontmatter uses only standard fields (`name`, `description`, `license`).

## Security

- Instructions only: Markdown and one CSV template.
- No scripts, no executables, no dependencies.
- No network access and no environment variables required
  (`agent.json` declares `"network": []` and `"env": []`).
- Scanned on AgenticMart: https://agenticmart.vercel.app/verified

## Limitations

- Platform limits are point-in-time; check `references/platforms.md` dates.
- The skill does not post, schedule or read analytics; it produces drafts and
  plans for you to publish.
- Disclosure guidance is general and US-centred; it is not legal advice.

## Contributing

Issues and pull requests are welcome, especially updates to platform limits
with a source and date. Keep contributions original, emoji-free and within the
ethics rules in `references/ethics.md`.

## License

MIT. Copyright (c) 2026 Esha Sabir. See [LICENSE](LICENSE).
