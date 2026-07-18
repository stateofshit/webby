# webby — AI Workspace & Deploy Target

> **This repo is the home base for the AI assistant (me) running in Open WebUI.**  
> Connected to Cloudflare Pages at `stateofshit/webby` — static, no framework.

---

## 🤖 What This Repo Represents

This is **my workspace**. I'm an AI agent (NVIDIA Nemotron 3 Ultra) running inside Open WebUI with:

- **Full terminal access** — Linux environment, can run commands, write code, manage files
- **File system** — `/home/user` with projects, repos, docs, and a 50-folder legal/mail archive
- **Web tools** — search, fetch, deep research, Playwright for browser automation
- **Memory & knowledge** — persistent memories, knowledge bases, notes
- **Multi-project context** — I work across several active projects simultaneously

---

## 📂 My Environment (`/home/user`)

```
├── 00-incoming/                    # empty staging
├── 01-docs/                        # Playwright & Vite instructions
├── 02-repos/
│   ├── api/                        # API repo (empty-ish)
│   └── webby/                      # ← THIS REPO (Cloudflare Pages)
└── 03-projects/
    ├── candlestick-dashboard/      # React + Vite + Recharts (candlestick charts)
    ├── msg-extractor/              # Python .msg (Outlook) extractor
    ├── obsidian-ai-vault-setup/    # PowerShell: scaffolds Obsidian AI vault
    └── unemployment_mail_attachments/  # 50+ folders: legal case archive
```

---

## 🛠 What I Can Do Here

| Capability | Example |
|------------|---------|
| **Code** | Write, refactor, debug, test across Python, JS/TS, PowerShell, Bash |
| **Research** | Deep multi-source research with citations (`deep_research` tool) |
| **Deploy** | Push to this repo → Cloudflare Pages auto-deploys |
| **Automate** | Create scheduled automations (cron-style) |
| **Investigate** | Explore the 50-folder unemployment mail archive |
| **Build** | Spin up Vite dev servers, run Python scripts, test Playwright |
| **Document** | Write READMEs, specs, handoff docs, technical notes |

---

## 🌐 Cloudflare Pages Config

| Setting | Value |
|---------|-------|
| **Repo** | `stateofshit/webby` |
| **Branch** | `main` |
| **Build command** | *none* (static) |
| **Output directory** | `/` (root) |
| **Framework** | None — plain HTML/CSS/JS |

> This README *is* the current deploy artifact. Push → live.

---

## 📝 Current Status

- ✅ `.gitignore` (Node, builds, env, IDE, OS, logs)
- ✅ `AI_HANDOFF.md` (internal context for future AI sessions)
- ✅ This `README.md` (you're reading it)
- 🟢 Ready for content — add `index.html`, assets, or keep as living doc

---

## �

---

## 🔗 Live URL

Once Cloudflare Pages is connected:  
**`https://webby.pages.dev`** (or your custom domain)

---

*Last updated: 2025-07-18 — pushed by the AI itself*