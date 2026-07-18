# Webby AI Handoff

This repository is owned by the `stateofshit` GitHub account and is intended to be connected to Cloudflare Pages.

## Purpose

Use this repo as the source for a Cloudflare Pages site. Future chat/model sessions should treat this as the deployable website repo, not as scratch space.

## Working Location

Inside Open Terminal:

```bash
cd ~/02-repos/webby
```

Host path:

```text
/home/ubuntu/openwebui/workspace/02-repos/webby
```

Git remote:

```text
git@github.com:stateofshit/webby.git
```

SSH auth for GitHub is already configured inside Open Terminal with:

```text
~/.ssh/github_openwebui
```

Do not replace that key unless GitHub auth stops working.

## Cloudflare Pages Expectations

When setting this up in Cloudflare Pages:

- Connect GitHub repo: `stateofshit/webby`
- Production branch: `main`
- Deploy from the repository root unless a framework later requires a subdirectory.
- If the site is static HTML/CSS/JS, use no build command and deploy the output/root directory directly.
- If a framework is added later, document the build command and output directory in this file.

Common framework settings:

```text
Plain static site:
  Build command: none
  Output directory: /

Vite:
  Build command: npm run build
  Output directory: dist

Next.js static export:
  Build command: npm run build
  Output directory: out
```

Only use the framework settings that match the actual project files.

## Git Workflow

Before changing anything:

```bash
git status
git pull --ff-only
```

After changes:

```bash
git status
git add .
git commit -m "Describe the change"
git push
```

If Git identity is missing inside Open Terminal, set it once:

```bash
git config --global user.name "stateofshit"
git config --global user.email "PUT_GITHUB_EMAIL_HERE"
```

## Rules For Future AI Work

- Keep deployable site files in this repo.
- Do not put private keys, API keys, `.env` secrets, exported account credentials, or OpenWebUI database files in this repo.
- If Cloudflare environment variables are needed, configure them in Cloudflare Pages, not in committed files.
- Prefer simple static output unless the requested site needs a framework.
- If a build system is added, update this file with the exact install/build/deploy details.
- Before finalizing changes, run the relevant local check:
  - Static site: inspect files and open locally if possible.
  - Node/Vite/etc.: run install/build checks if dependencies are present.
- Do not force-push unless the user explicitly asks for it.

## Current State

At creation, this repo only had a minimal `README.md`. No Cloudflare Pages project settings have been committed yet.
