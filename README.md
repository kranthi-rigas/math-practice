# Math Practice (K–3rd Grade) — Installable PWA

A colorful, kid-friendly **intelligent** math practice app for Kindergarten through 3rd grade. No login. Works fully offline after the first load, and can be installed to the home screen on iPad, iPhone, and Android.

- **Grade picker** on the home screen (K · 1st · 2nd · 3rd), remembered on the device. Defaults to **2nd grade**
- Every question is **generated randomly** (no fixed quiz list), avoiding recent repeats
- **Countdown timer** on each question (15 / 25 / 30 / 45s, set on the home screen and remembered)
- **Pictures where they help**: emoji groups, ten-frames, base-ten blocks, analog clocks (SVG), coins and bills, rulers, fraction bars and circles, number lines, rectangles and L-shapes
- **Answer box is focused automatically** on every typed question (round start, next question, retry, after time-up), with the text selected for easy retyping. Number answers show a **number pad** (`inputmode="numeric"`); expanded-form answers get the normal keyboard (they need `+`). **Enter** checks the answer, and Enter again goes to the next question. Picture/clock/fraction questions use big **tap buttons** instead.

## Grades and modes (levels 1–10 each)

**Kindergarten**
- **Counting:** L1 up to 5 in a row → L3–5 ten-frame rows and scattered pictures → L6–8 up to 20 → L9–10 count only one kind among two
- **Before & After:** L1–3 after/before within 10 → L4–6 within 20–30, "in the middle" → L7–10 up to 100, counting by tens
- **More or Fewer:** L1–4 compare two picture groups (more, fewer, same) → L5–6 bigger/smaller number → L7–10 messier groups, "same", biggest/smallest of three
- **Add & Subtract:** L1–4 within 5 then 10 with pictures (take-away pictures crossed out) → L5–6 numbers only → L7 make 10 with a ten-frame → L8 missing numbers → L9–10 tiny stories
- **Shapes (tap):** L1–2 find/name circle, square, triangle, rectangle, hexagon → L3–4 sides and corners → L5 cube, sphere, cylinder, cone and real objects → L6 flat or solid → L7 rotated shapes → L8 count shapes in a row → L9–10 "which has 6 sides?"

**1st grade**
- **Add & Subtract:** L1–2 within 10 → L3–4 teens without crossing 10 → L5–6 crossing 10 → L7 missing addend → L8 three addends → L9–10 two-digit + ones/tens, tens − tens
- **Tens & Ones:** L1–3 count base-ten blocks (to 99) → L4–6 tens/ones in a number → L7–8 10 more / 10 less → L9 scrambled "5 ones and 6 tens" → L10 numbers to 120
- **Compare Numbers (< > =):** L1–2 within 10/20 → L3–5 two-digit, close, same tens → L6 "3 tens 4 ones vs 43" → L7–8 up to 120 → L9–10 "40 + 3 vs 44"
- **Word Problems:** L1–4 add/subtract stories within 10 then 20 → L5 how many more → L6–7 change/start unknown → L8 three addends → L9–10 fewer / how many more needed
- **Telling Time (tap, analog clock):** L1–2 o'clock → L3 half past → L4–5 pick the clock → L6 "half past 4" = 4:30 → L7–8 1 hour / half hour later → L9–10 schedule stories

**2nd grade** (the original four modes keep their levels exactly as before, plus four new ones)
- **Addition & Subtraction · Place Value · Number Comparison · Word Problems:** unchanged from v2/v3 (see table below)
- **Money:** L1–4 count pennies/nickels/dimes/quarters (values shown) → L5–6 coin names only, mixed order → L7 $1/$5/$10 bills → L8 "you buy a toy, how much is left?" → L9 how much more to make $1 → L10 mixed incl. coin word problems
- **Telling Time (tap):** L1–2 hour, half hour, quarter past/to → L3–4 any 5 minutes → L5 pick the clock → L6 10/15/20 minutes later → L7 minutes after the hour (typed) → L8 a.m./p.m. → L9–10 30 minutes later across the hour, mixed
- **Skip Counting & Rulers:** L1–3 by 10s, 5s, 2s → L4 by 10s from any number → L5 by 100s → L6–7 by 5s/2s/10s/100s up to 1000 → L8 measure a pencil in inches → L9 measure in cm (not starting at 0) → L10 mixed incl. counting backward and "how much longer?"
- **Even, Odd & Arrays:** L1 pairs pictures → L2–3 numbers to 20 → L4 pairs to 20 → L5 doubles (? + ? = 14) → L6 two-digit even/odd → L7 arrays (rows of) → L8 repeated addition → L9 three-digit → L10 mixed

**3rd grade**
- **Multiplication:** L1 ×0/1/2 → L2 ×2/5/10 → L3 ×3 → L4 ×4 → L5 arrays → L6 ×6/7 → L7 ×8/9 → L8 all facts to 10×10 → L9 missing factor → L10 × multiples of 10, mixed
- **Division:** L1 ÷1/2 → L2 ÷5/10 → L3 ÷3/4 → L4 sharing pictures → L5 ÷6/7 → L6 ÷8/9 → L7 all facts → L8 missing dividend → L9 missing divisor → L10 mixed incl. 0 and 1 rules
- **Add, Subtract & Round:** L1–3 round to nearest 10 (2- and 3-digit) and 100 → L4–5 3-digit without regrouping → L6–7 with regrouping (incl. across zeros) → L8 estimate by rounding → L9 missing numbers → L10 mixed
- **Fractions (tap):** L1 unit fractions from a picture → L2 "what fraction is shaded?" → L3 pick the picture → L4–5 fractions on a number line → L6 compare, same denominator → L7 compare, same numerator → L8 equivalent fractions → L9 whole numbers as fractions, number line to 2 → L10 mixed
- **Time & Elapsed Time:** L1–3 read clocks to 5 minutes then to the minute → L4 pick the clock → L5 elapsed minutes within an hour → L6 end time → L7 elapsed across the hour → L8 start time → L9 elapsed between two clocks → L10 mixed incl. over an hour
- **Area & Perimeter:** L1–2 count unit squares → L3 area from side lengths → L4–5 perimeter (grid, then labels) → L6 area or perimeter → L7–8 missing side from area/perimeter → L9 L-shaped area → L10 mixed
- **Word Problems:** L1–4 equal groups, sharing, arrays, teams → L5 3-digit stories → L6 money × ÷ → L7–9 two-step → L10 mixed

## Levels (1–10 per mode)

The **next** question's level depends on how the **current** one went:

| Result | Level change |
|---|---|
| Correct on first try, fast (under 1/3 of the time limit) | **+2** |
| Correct on first try | **+1** |
| Correct on the second try | stays the same |
| Wrong twice, or time ran out | **−1** |

Levels are clamped to 1–10 and remembered **per grade and mode** on the device.

Original 2nd-grade modes:
- **Add/Sub:** L1 within 10 → L3 within 20 crossing 10 → L6 2-digit with regrouping → L7 missing numbers → L10 3-digit ± 3-digit with regrouping
- **Place value:** L1–2 tens/ones → L3–6 hundreds, expanded form, 10 more → L7–8 zeros, scrambled places, 10/100 more/less → L9–10 thousands
- **Comparison:** L1 2-digit far apart → L3 close 2-digit → L4–7 3-digit, same hundreds, swapped digits → L8 "40 + 5 □ 44" → L9–10 4-digit and expanded form
- **Word problems:** L1 add within 10 → L5–6 within 100, "how many more" → L7 missing part → L8–9 two-step → L10 two-step or 3-digit stories

## Scoring (competitive)

- Points = **10 × level** + **speed bonus** (up to +20, based on time left) × **streak multiplier**
- Streak of first-try correct answers: **×1.5** at 3 in a row, **×2** at 5+
- Correct on second try: half of 10 × level (no bonus). Wrong / timeout: 0 and streak resets
- Rounds are **10 questions**, then a summary: score, accuracy, highest level, best streak, best score
- **Best score per grade + mode** is saved on the device (localStorage) with a 🎉 *New best!* celebration

## Saved progress

Keys: `mp_grade`, `mp_time`, `mp_best_<grade>_<mode>`, `mp_level_<grade>_<mode>` (e.g. `mp_best_2_addsub`, `mp_level_K_count`).
Versions 1–3 saved 2nd-grade progress as `mp_best_<mode>` / `mp_level_<mode>`; v4 copies those to the 2nd-grade keys once on first launch (never overwriting newer data) and leaves the old keys in place.

## Adding a grade (4th, 5th…)

In `index.html`: write one generator per mode (`function genG4Something(level) { … return problem; }` for levels 1–10), then add an entry to `GRADES` and its key to `GRADE_ORDER`. The grade chip, tiles, saving, levels, and scoring all come from the registry. A problem is an object like
`{ html, answer, displayAnswer, inputType: "number" | "text" | "choice" | "compare", choices?, key }` (helpers: `numQ`, `choiceQ`, `compareQ`, plus the SVG helpers for clocks, coins, fractions, rulers, rectangles).

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

> iOS note: Safari only opens the keyboard when focus comes from a tap. If the keyboard is closed and a question auto-advances after time runs out, tap the answer box (on Android/desktop it focuses and opens automatically).


When you change any file, bump `CACHE_VERSION` in `service-worker.js` (currently `math-practice-v4`) so devices pick up the new version (it takes effect on the next launch after an online visit).
