---
title: Skills by Vercel Labs
---

# Skills: give your AI agent the skills it's missing 🧠

Don't go to your next hackathon without this. Ask an AI coding agent to build a front end or plan an architecture without the right context and you get generic output. **Skills** (from Vercel Labs) is an open-source CLI and directory of agent skills: reusable instructions your agent loads when it needs them.

| | |
|---|---|
| 🔗 Repo | [github.com/vercel-labs/skills](https://github.com/vercel-labs/skills) |
| 📚 Directory | [skills.sh](https://skills.sh) |
| ⭐ The one to start with | [find-skills](https://skills.sh/vercel-labs/skills/find-skills), #1 on the skills.sh leaderboard |

## Step 1: Install find-skills

find-skills lets your agent search the skills directory for you, so you don't have to hunt on your own:

```bash
npx skills add https://github.com/vercel-labs/skills --skill find-skills
```

Then just ask your agent things like "find a skill for frontend design" or "is there a skill for testing?".

## Step 2: Or search yourself

```bash
npx skills find design
npx skills find testing
npx skills find video
```

You can also search on [skills.sh](https://skills.sh) and install with `npx skills add <owner/repo>`.

## A starter set for a hackathon

- **Design:** a frontend/UI design skill, so the agent's screens stop looking generic.
- **Testing:** a web-app testing skill, so it checks the main flow before your demo.
- **Demo video:** a video skill, if you want the agent to help make your demo or launch video.

Pick by install count and source: official sources (Vercel, Anthropic and the tool makers themselves) first. Read a skill's SKILL.md before you install it.

## Tips

- Install skills the night before, not during the build.
- Fewer, better skills beat twenty random ones.
- Works with the major coding agents; check the repo's README for the current list.

---

Last checked: 27 Oct 2026. Install counts and rankings change daily.

Follow [@souradip.sh](https://www.instagram.com/souradip.sh/) for hackathon tips every day.
