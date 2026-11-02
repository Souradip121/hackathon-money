---
title: 7 GitHub Repos That Replace Paid Dev Tools
---

# 7 GitHub repos that replace paid dev tools 🛠️

Your whole hackathon stack, open source. Each one has a free way to start in under 5 minutes, and a way to self-host it when you want to own your data.

| Repo | Use it for | Instead of |
|---|---|---|
| Hoppscotch | Testing APIs | Postman, Insomnia |
| Penpot | Design and prototypes | Figma |
| Plane | Issues, cycles, boards | Jira, Linear |
| Formbricks | Surveys and user feedback | Typeform |
| Uptime Kuma | Monitoring your demo | UptimeRobot |
| Excalidraw | Architecture diagrams | Miro |
| Dokploy | Deploying apps and databases | Vercel, Netlify, Heroku |

## 1. Hoppscotch: test your APIs

- **Repo:** [github.com/hoppscotch/hoppscotch](https://github.com/hoppscotch/hoppscotch) (MIT)
- **Fastest start:** open [hoppscotch.io](https://hoppscotch.io) in your browser. Nothing to install. Desktop apps exist too.
- **Self-host:** [the self-hosting guide](https://docs.hoppscotch.io/documentation/self-host/getting-started).

## 2. Penpot: design your app

- **Repo:** [github.com/penpot/penpot](https://github.com/penpot/penpot) (MPL-2.0)
- **Fastest start:** a free account at [design.penpot.app](https://design.penpot.app). Your designer and your devs work in the same file.
- **Self-host:** Docker and other options at [penpot.app/self-host](https://penpot.app/self-host).

## 3. Plane: plan the sprint

- **Repo:** [github.com/makeplane/plane](https://github.com/makeplane/plane) (AGPL-3.0)
- **Fastest start:** a free account on [Plane Cloud](https://app.plane.so).
- **Self-host:** the [deployment guides](https://developers.plane.so/self-hosting/overview).

## 4. Formbricks: get user feedback

- **Repo:** [github.com/formbricks/formbricks](https://github.com/formbricks/formbricks) (AGPL-3.0 core; one enterprise folder is commercial)
- **Fastest start:** the free cloud plan at [app.formbricks.com](https://app.formbricks.com/auth/signup).
- **Hackathon move:** send a 3-question survey to 20 real users before the finale, and walk in with their answers. Judges always ask "who will actually use this?"

## 5. Uptime Kuma: keep your demo alive

- **Repo:** [github.com/louislam/uptime-kuma](https://github.com/louislam/uptime-kuma) (MIT)
- **Start it with one command** (needs Docker):

```
docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:2
```

- Open `http://localhost:3001`, add your demo URL, and connect Telegram or Discord alerts. You'll know your demo is down before a judge does.

## 6. Excalidraw: draw the architecture

- **Repo:** [github.com/excalidraw/excalidraw](https://github.com/excalidraw/excalidraw) (MIT)
- **Fastest start:** [excalidraw.com](https://excalidraw.com). Hand-drawn boxes and arrows, live collaboration with your team, export to PNG or SVG for your slides.

## 7. Dokploy: deploy it

- **Repo:** [github.com/Dokploy/dokploy](https://github.com/Dokploy/dokploy) (Apache-2.0, except one proprietary folder)
- **Self-host on a VPS** with one command:

```
curl -sSL https://dokploy.com/install.sh | bash
```

- Then deploy apps and databases from one dashboard. Want to skip the server? There's [Dokploy Cloud](https://app.dokploy.com).

---

All seven were checked on GitHub on 2 Nov 2026: open source, not archived, and with commits in the last week. Cal.com isn't on this list any more: it moved to closed source in April 2026.

Follow [@souradip.sh](https://www.instagram.com/souradip.sh/) for hackathon tips every day.
