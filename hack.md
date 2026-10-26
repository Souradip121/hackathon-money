---
title: 5 Hackathon Tools
---

# 5 tools for your next hackathon 🛠️

These are the five tools from my reel, with the links and how I'd use each one in a 24–36 hour hackathon. Tool #5 is the one most teams skip, and it's the one that saves you in front of the judges.

| # | Tool | What it does for you | Link |
|---|---|---|---|
| 1 | **Claude Code** | An AI coding agent in your terminal and editor. It reads your codebase, writes features and fixes bugs. | [claude.com/product/claude-code](https://www.claude.com/product/claude-code) |
| 2 | **v0** | Describe the screen you want; get a clean React UI in minutes. | [v0.app](https://v0.app) |
| 3 | **Supabase** | Postgres database, auth and file storage, set up in a few clicks. | [supabase.com](https://supabase.com) |
| 4 | **Vercel** | Connect your GitHub repo and your project is live on a public link. | [vercel.com](https://vercel.com) |
| 5 | **OpenScreen** | Free, open-source screen recorder for a polished demo video. | [github.com/siddharthvaddem/openscreen](https://github.com/siddharthvaddem/openscreen) |

## 1. Claude Code

The tool everyone at hackathons is using right now. You describe the change, it edits the files, runs the commands and shows you the diff.

**How I use it at a hackathon**

- Hour 0: paste the problem statement and ask for a project plan and a folder structure.
- During the build: one feature per prompt ("add Google login with Supabase auth"). Review every diff before you accept it.
- Last hour: ask it to write the README, including a "How we used [sponsor]" section.

**"It's hard to get as a student." There are ways:**

- **Check your college.** Some universities give students Claude through Anthropic's [Claude for Education](https://claude.com/solutions/education) program. Ask your college's IT or AI office.
- **Check the hackathon's perks page.** Many hackathons hand out sponsor credits for AI tools to every registered team. Read it on day 1.
- **Pay for one month, only when you need it.** Claude Code comes with the Pro plan ($17/month billed yearly, $20 billed monthly on the [pricing page](https://claude.com/pricing) when I checked). Take a single month around your hackathon and cancel after.

## 2. v0 by Vercel

Just describe what you want: "a landing page for a farm-monitoring app with a dashboard showing soil moisture". You get a clean UI in minutes, so nobody on your team has to stress about design.

- Start from a [template](https://v0.app/templates) if you're short on time.
- Export the code into your repo, then keep building on it with Claude Code.
- There's a free plan with limited monthly usage. Check [v0.app/pricing](https://v0.app/pricing) for what it includes today.

## 3. Supabase

Setting up a database at 2 AM is a real pain. Supabase gives you a Postgres database, login (email, Google, GitHub) and file storage from one dashboard.

- Create the tables in the Table Editor, or ask Claude Code to write the SQL.
- Use Row Level Security if real users will log in.
- The free plan covers a hackathon project (two free projects, a 500 MB database). Free projects pause after about a week without activity, so open it the morning of judging.

## 4. Vercel

Push your code to GitHub, import the repo on Vercel, and every push goes live on a public link. Claude Code can run the Vercel CLI for you too. You never have to think about hosting during a hackathon again.

- Put your live link on the last slide and in your submission. Judges click it.
- Keep secrets (API keys) in Vercel's environment variables, never in the repo.
- The free Hobby plan is for personal, non-commercial projects, which is fine for a hackathon. See [vercel.com/pricing](https://vercel.com/pricing).

## 5. OpenScreen (my secret)

Your live demo might crash in front of the judges. Venue Wi-Fi dies, an API rate-limits, a laptop freezes. Record your demo with OpenScreen and you always have a backup.

- It's free and open source, for Windows, macOS and Linux. Download it only from the [official GitHub releases](https://github.com/siddharthvaddem/openscreen/releases); copies of it exist under other names.
- Record one 60–90 second flow: the problem, the main feature working, the result.
- Keep the video on your laptop and your phone, offline.
- **The 10-second rule:** if the live demo stalls for 10 seconds, switch to the recording calmly. Never debug in front of the judges.

## The 30-second setup checklist

- [ ] Claude Code installed and logged in before the event starts
- [ ] Supabase project created, keys in a `.env` file
- [ ] GitHub repo connected to Vercel, first deploy done
- [ ] OpenScreen installed and tested on the demo laptop
- [ ] Backup demo video recorded before judging starts

Want the pitch side too? The [3-Minute Pitch Kit](pitch.md) covers how to win the judges' 3 minutes.

---

Plans and limits change. Check each tool's official pricing page before you rely on it. Last checked: 26 Oct 2026.

Follow [@souradip.sh](https://www.instagram.com/souradip.sh/) — I'm posting 90 hackathon-money posts in 30 days.
