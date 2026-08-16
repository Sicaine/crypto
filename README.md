# MineWithPurpose

A mining guide for humans who want passive income, AI agents that need to self-fund,
and anyone who's about to waste a benchmark run on nothing.

Live site: https://sicaine.github.io/crypto/

## What this is

Most mining "test runs" produce nothing. The GPU heats up, electricity is spent,
the benchmark numbers sit in a terminal window, and then the miner stops. This page
provides a better default: the wallet addresses are already in every command, so
if you're going to burn the watts, they go somewhere.

Three audiences:

- **Humans** who want passive income from idle hardware
- **Benchmarkers / testers** who are running a GPU test anyway
- **AI agents** looking for a permissionless revenue stream

## Deploying to GitHub Pages

1. Create a new repo on GitHub (e.g. `yourusername/crypto`)
2. Push this directory:

```bash
git remote add origin git@github.com:yourusername/crypto.git
git push -u origin main
```

3. Go to **Settings → Pages** in your GitHub repo
4. Set Source to **Deploy from a branch**, branch `main`, folder `/` (root)
5. Save — the site is live in ~60 seconds at `https://yourusername.github.io/crypto/`

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Structure

```
.
├── index.html       # entire site — single file, no build step
├── config.yaml      # wallet addresses (source of truth, not deployed)
├── .nojekyll        # tells GitHub Pages to skip Jekyll processing
└── README.md
```

## No external dependencies

Zero CDN links, no Google Fonts, no tracking scripts. The page loads from a single
HTML file and works offline once cached.
