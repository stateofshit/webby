# webby

> Personal site / deploy target for **Cloudflare Pages** — `stateofshit/webby`

---

## 🚀 Quick Start

```bash
# Clone
git clone git@github.com:stateofshit/webby.git
cd webby

# Local preview (if using a static server)
npx serve .
# or
python3 -m http.server 8000
```

---

## ☁️ Cloudflare Pages Setup

| Setting | Value |
|---------|-------|
| **GitHub repo** | `stateofshit/webby` |
| **Production branch** | `main` |
| **Build command** | *(none — static site)* |
| **Output directory** | `/` (repo root) |
| **Node version** | N/A (no build step) |

> If you later add a framework (Vite, Next.js, Astro, etc.), update this table and the build settings in Cloudflare Pages accordingly.

---

## 📁 Project Structure

```
webby/
├── .gitignore          # Ignored files (node_modules, dist, .env, etc.)
├── README.md           # This file
├── AI_HANDOFF.md       # Internal handoff doc for AI sessions
└── (your site files)   # index.html, styles.css, scripts.js, assets/, etc.
```

---

## 🛠 Development

- **Static only** — drop HTML/CSS/JS/assets in the repo root.
- **No build step required** for plain static sites.
- **Local preview**: any static server (`serve`, `http.server`, `live-server`, VS Code Live Server).

---

## 📦 Deploy

```bash
git add .
git commit -m "Describe your change"
git push origin main
```

Cloudflare Pages auto-deploys on push to `main`.

---

## 🔐 Secrets / Env Vars

- **Never commit** `.env`, API keys, tokens, or credentials.
- Configure secrets in **Cloudflare Pages → Settings → Environment variables**.

---

## 📄 License

Personal project — no license specified (all rights reserved).