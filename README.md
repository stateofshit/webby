# webby

**Static site repository for Cloudflare Pages** — `stateofshit/webby`

## Purpose

This repo serves as the deploy target for a Cloudflare Pages site. No framework, no build step — plain HTML/CSS/JS assets served from the repository root.

## Deployment

| Setting | Value |
|---------|-------|
| **Provider** | Cloudflare Pages |
| **Repository** | `git@github.com:stateofshit/webby.git` |
| **Branch** | `main` |
| **Build command** | *(none)* |
| **Output directory** | `/` (repo root) |
| **Node version** | N/A |

**Deploy trigger:** Push to `main` → automatic build + deploy.

## Project Structure

```
webby/
├── .gitignore          # Standard ignores (node_modules, dist, .env, IDE, OS)
├── README.md           # This file
├── AI_HANDOFF.md       # Internal context for AI sessions
└── [site assets]       # index.html, styles.css, script.js, images/, etc.
```

## Local Development

```bash
# Clone
git clone git@github.com:stateofshit/webby.git
cd webby

# Preview locally (any static server)
npx serve .
# or
python3 -m http.server 8000
# or
php -S localhost:8000
```

## Adding Content

Drop static files in the repo root:

```
webby/
├── index.html          # Required for root path
├── styles.css
├── app.js
├── favicon.ico
├── assets/
│   ├── images/
│   └── fonts/
└── other-page.html     # Accessible at /other-page.html
```

**No build step.** Edit → commit → push → live.

## Environment Variables / Secrets

**Never commit secrets.** Configure in Cloudflare Pages dashboard:

```
Settings → Environment variables → Add variable
```

| Variable | Purpose |
|----------|---------|
| `API_KEY` | External API credentials |
| `ANALYTICS_ID` | Analytics/tracking IDs |
| `FEATURE_FLAG_*` | Runtime toggles |

## Git Workflow

```bash
# Before work
git status
git pull --ff-only

# After changes
git add .
git commit -m "Describe the change"
git push origin main
```

**No force-push** unless explicitly requested.

## Custom Domain (Optional)

In Cloudflare Pages:
1. **Custom domains** → **Set up a custom domain**
2. Add `webby.yourdomain.com` (or apex)
3. Cloudflare manages DNS if zone is on Cloudflare; otherwise add CNAME manually.

## SSL / Headers / Redirects

Configure in Cloudflare Pages dashboard or add a `_headers` / `_redirects` file to repo root:

```text
# _headers
/*
  X-Frame-Options: DENY
  X-Content-Type-Options: nosniff
  Referrer-Policy: strict-origin-when-cross-origin

# _redirects
/old-page.html  /new-page.html  301
/blog/*         /articles/:splat  301
```

## License

Private repository — no license granted. All rights reserved.