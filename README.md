# Math Practice (2nd Grade) — Installable PWA

A colorful, kid-friendly **intelligent** math practice app for second grade. No login. Works fully offline after the first load, and can be installed to the home screen on iPad, iPhone, and Android.

- Every question is **generated randomly** (no fixed quiz list), avoiding recent repeats
- **Countdown timer** on each question (15 / 25 / 30s, set on the home screen and remembered)
- 4 modes: Addition & Subtraction · Place Value · Number Comparison · Word Problems

## Levels (1–10 per mode)

The **next** question's level depends on how the **current** one went:

| Result | Level change |
|---|---|
| Correct on first try, fast (under 1/3 of the time limit) | **+2** |
| Correct on first try | **+1** |
| Correct on the second try | stays the same |
| Wrong twice, or time ran out | **−1** |

Levels are clamped to 1–10 and remembered per mode on the device.

- **Add/Sub:** L1 within 10 → L3 within 20 crossing 10 → L6 2-digit with regrouping → L7 missing numbers → L10 3-digit ± 3-digit with regrouping
- **Place value:** L1–2 tens/ones → L3–6 hundreds, expanded form, 10 more → L7–8 zeros, scrambled places, 10/100 more/less → L9–10 thousands
- **Comparison:** L1 2-digit far apart → L3 close 2-digit → L4–7 3-digit, same hundreds, swapped digits → L8 "40 + 5 □ 44" → L9–10 4-digit and expanded form
- **Word problems:** L1 add within 10 → L5–6 within 100, "how many more" → L7 missing part → L8–9 two-step → L10 two-step or 3-digit stories

## Scoring (competitive)

- Points = **10 × level** + **speed bonus** (up to +20, based on time left) × **streak multiplier**
- Streak of first-try correct answers: **×1.5** at 3 in a row, **×2** at 5+
- Correct on second try: half of 10 × level (no bonus). Wrong / timeout: 0 and streak resets
- Rounds are **10 questions**, then a summary: score, accuracy, highest level, best streak, best score
- **Best score per mode** is saved on the device (localStorage) with a 🎉 *New best!* celebration

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
