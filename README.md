# Rishabh Karthik Ramesh — Portfolio

A single-file, zero-build portfolio site. Dark theme, live GitHub feed, deploys on Vercel in ~1 minute.

## Quick edit (1 thing to do)

Open `index.html`, scroll to the bottom, and edit the `CONFIG` block:

```js
const CONFIG = {
  githubUsername: "RishCapitalent18",
  linkedinUrl:    "https://www.linkedin.com/in/rishabh-karthik-ramesh/",
  resumePath:     "Resume.pdf",
  photoPath:      "profile.jpg"
};
```

- **githubUsername** — drives the live "Latest from GitHub" feed and all repo links.
- **linkedinUrl** — your real LinkedIn profile URL.
- **resumePath** — drop your resume PDF into this folder named `Resume.pdf` (or change the path) so the Resume buttons work.
- **photoPath** — drop a **square headshot** into this folder named `profile.jpg` (JPG or PNG). It appears in the hero with a glowing ring. If the file is missing, the photo area hides itself automatically, so the layout still looks clean.

> The three flagship project cards link to your GitHub profile by default. To point a card at a specific repo, set its `data-repo="repo-name"` attribute in the HTML (the Agentic RAG card already targets `agentic-rag-filings`).

## Deploy on Vercel

### Option A — drag & drop (fastest)
1. Go to [vercel.com/new](https://vercel.com/new).
2. Drag this `portfolio` folder onto the page (or use the "deploy" upload).
3. Done — you get a live `*.vercel.app` URL.

### Option B — GitHub + Vercel (recommended, auto-redeploys)
1. Create a new GitHub repo (e.g. `portfolio`) and push this folder:
   ```bash
   git init
   git add .
   git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/<you>/portfolio.git
   git push -u origin main
   ```
2. At [vercel.com/new](https://vercel.com/new), **Import** the repo.
3. Framework preset: **Other** (it's static — no build step). Click **Deploy**.
4. Every future `git push` to `main` auto-redeploys.

### Custom domain (optional)
Vercel → Project → **Settings → Domains** → add your domain and follow the DNS instructions. Or just use the free `yourname.vercel.app`.

## Files
- `index.html` — the entire site (HTML + CSS + JS).
- `vercel.json` — clean URLs + basic security headers.
- `Resume.pdf` — add this yourself so the Resume buttons download it.
