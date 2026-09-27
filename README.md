# Math Practice (2nd Grade) — Installable PWA

A colorful, kid-friendly **intelligent** math practice app for second grade. No login. Works fully offline after the first load, and can be installed to the home screen on iPad, iPhone, and Android.

- Every question is **generated randomly** (no fixed quiz list)
- **Countdown timer** on each question (15 / 25 / 30s, set on the home screen)
- **Adaptive difficulty**: harder after streaks, easier after misses
- 4 modes: Addition & Subtraction · Place Value · Number Comparison · Word Problems

## Files

```
index.html              app (HTML + CSS + JS, self-contained)
manifest.webmanifest    PWA manifest (name, icons, colors, standalone)
service-worker.js       offline cache (cache-first, versioned)
icons/                  192, 512, maskable 512, 180 apple-touch, 32 favicon
```

All paths are relative, so it works at a domain root or under a subpath (e.g. `https://you.github.io/math-practice/`).

## Run locally

```bash
cd math-practice-app
python3 -m http.server 8765
```

Open http://localhost:8765/ (opening `index.html` directly also works, but offline caching / install need http(s)).

## Install on a device

Service workers and install **require HTTPS** (localhost is the only exception). Host the folder on any static HTTPS host (GitHub Pages, Netlify, Cloudflare Pages…), then:

- **iPad / iPhone (Safari):** Share button → **Add to Home Screen**.
- **Android (Chrome):** menu ⋮ → **Install app** / **Add to Home screen**.

After the first visit, the app works with no internet.

## Updating

When you change any file, bump `CACHE_VERSION` in `service-worker.js` (e.g. `math-practice-v2`) so devices pick up the new version (it takes effect on the next launch after an online visit).
