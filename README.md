# Math Practice (K–5th Grade) — Installable PWA

A colorful, kid-friendly **intelligent** math practice and learning app for Kindergarten through 5th grade. No login. Works fully offline after the first load, and can be installed to the home screen on iPad, iPhone, and Android.

- **Grade picker** on the home screen (K · 1st · 2nd · 3rd · 4th · 5th), remembered per kid. Defaults to **2nd grade**
- Every question is **generated randomly** (no fixed quiz list), avoiding recent repeats
- **Countdown timer** on each question (15 / 25 / 30 / 45s, set on the home screen and remembered)
- **Pictures where they help**: emoji groups, ten-frames, base-ten blocks, analog clocks (SVG), coins and bills, rulers, fraction bars and circles, number lines, rectangles and L-shapes
- **Answer box is focused automatically** on every typed question (round start, next question, retry, after time-up), with the text selected for easy retyping. Number answers show a **number pad** (`inputmode="numeric"`); expanded-form answers get the normal keyboard (they need `+`). **Enter** checks the answer, and Enter again goes to the next question. Picture/clock/fraction questions use big **tap buttons** instead.

## Learning features (v6)

- **📘 Learn mode**: pick the 📘 Learn game type on home, then tap any topic. Each of the 42 topics has a short picture lesson (3–5 screens), such as base-ten blocks for regrouping, fraction bars, clock hands, area models, long-division steps, bar models for word problems, or the coordinate grid. After the lesson come 3 guided "your turn" questions (levels 1, 2, 3). They have no timer, the hint shows right away, and every answer gets a worked explanation. Guided questions never change her saved level. Finishing a lesson the first time earns 1 ⭐, and home shows "Lesson done ✓" on the tile.
- **💡 Hint button** on Practice, Boss and review questions: a nudge that fits the question (e.g. "Line up the ones. 7 + 8 is more than 9, so regroup"). Using a hint is gentle. The question is worth half points, and a hinted answer can't count as "super fast" (+1 level instead of +2). It doesn't break the streak. Beat the Clock has no hints.
- **📖 Step-by-step explanations**: after a miss or a time-up, the card shows "How to solve it" steps built for *that* question. Examples: column addition with the carried 1, counting on, reading the hour and minute hands, making equal denominators, the long-division steps, or place-value tables. On a time-up the question still moves on by itself after 2.5 s like before, unless she taps **✋ Wait, I'm reading** (or the 🔈 on the steps).
- **🔁 Mistake review (spaced repetition)**: every missed question is saved for that kid (grade, mode, level, and the full question). The rules:
  - It comes back **1 day later**.
  - Right once: it comes back **3 days later** (or **7 days** if she missed it again during review).
  - Right **twice**: it's cleared (🔧 "Fixed for good!").
  - Missed during review: it comes back the next day.

  Due questions are mixed into Practice rounds of the same grade and mode (as question 4 and question 8, marked "🔁 One to fix from before!"). A **🔁 Fix my mistakes (N)** button appears on home whenever any are due, for an untimed review round (up to 10) that doesn't change levels. Up to 60 mistakes are kept per kid.
- **🗣️ Read-aloud**: a 🔈 button on each question, lesson page, and explanation reads it with the device voice (Web Speech API `speechSynthesis`). Math is spoken naturally: "plus", "minus", "times", "divided by", "is greater than", "3 fourths", "2 and 1 half", "7 tens", 3:45 as "three forty-five", $4.25 as "4 dollars and 25 cents", and "what number" for a blank. **Auto-read** is on for K and 1st by default (the parent can set Always / K & 1st / Never). Speech only starts after her first tap, as iOS requires. If the device has no speech support, the speaker buttons are hidden and nothing else changes.
- **👥 Kid profiles**: several children on one device, each with their own name, buddy, grade, levels, bests, stars, stickers, badges, daily goal and streak, mistakes, settings and stats.
  - When 2+ kids exist, a **"Who is playing?" picker** opens at launch. Tap the name chip on home to switch or **➕ Add a kid**; ⚙️ edits the current kid.
  - Deleting a kid is done in the parent dashboard, so it needs the PIN, and it asks for a second tap to confirm.
- **👪 Parent dashboard** (👪 on home, or "Grown-ups" on the picker), behind a **4-digit PIN**:
  - The PIN is created on first open and typed twice. It's saved as a hash, not in plain text.
  - **Forgot the PIN?** Answer a grown-up math question (like 47 × 23 + 518), then choose a new PIN.
  - Per kid, the dashboard shows:
    - time spent, rounds, questions answered, accuracy
    - stars and mistakes waiting
    - a **last-7-days chart** (questions per day with the right-answer share and minutes)
    - **strong topics** (≥ 85%) and **needs practice** (< 70%), using topics with 5+ questions
    - an **accuracy + level + best table** for each grade and topic
    - the **most-missed question types**
    - badges and stickers
  - **Settings per kid**: daily goal (1–5 rounds), default timer, allowed grades (the others are hidden from the grade picker), sounds on/off, read-aloud on/off, and auto-read.
  - **🖨️ Weekly summary**: a print-friendly page (totals, day by day, topics this week with levels, strengths, most-missed types, new badges). Print or "Save as PDF" from it.

## Fun stuff (v5)

- **Name & buddy**: on first launch the app asks for her name and a buddy animal (🐶 🐱 🐰 🐼 🦊 🐸 🦄 🐨). The buddy greets her by name on home and summary screens. Change it any time with ⚙️ on the home screen.
- **Game types** (pick on home; **Practice** is the default each time the app opens):
  - 🎯 **Practice**: the classic 10-question round.
  - ⏱️ **Beat the Clock**: 60 seconds, as many as she can. Levels still adapt. It keeps its own best for each grade and mode.
  - 👾 **Boss Round**: a boss monster with an HP bar (8 HP). Each right answer hits it (a super-fast answer hits 2). A miss or time-up lets the boss attack one of her 3 hearts. There's a win screen and a try-again screen.
- **Stars**: 1–3 per round.
  - Practice: 9+ right = 3, 6+ = 2.
  - Beat the Clock: 15+ = 3, 8+ = 2.
  - Boss: a win with all hearts = 3, any other win = 2, a loss = 1.
  - New players get 3 welcome stars.
- **Sticker book**: 36 emoji animal stickers (20 Common, 10 Rare, 6 Super Rare). Opening a surprise egg costs 3 ⭐. The egg shakes, then reveals a sticker she doesn't have yet. Rare ones come up less often.
- **Buddy mascot** on the question screen. It sits above the timer, so it never covers the question or the keyboard. It cheers right answers, encourages after misses, gets excited on streaks, and celebrates on the summary.
- **Sounds**: made with the Web Audio API, so there are no sound files and they work offline. Ding (right), soft buzz (miss), chime (streaks), jingle (level up), fanfare (new best, boss win, new badge), a soft click on taps, plus boss hit/attack and egg sounds. Audio only starts after the first tap, as iOS requires. The 🔊/🔇 button (home and question screens) is remembered on the device.
- **Badges** (🏅 screen): First Round, Speedy, Streak 5, Streak 10, Perfect Round, Level 10 Hero (one per grade), Explorer (every mode in a grade), Clock Champ, Boss Beater, Boss Master, Daily Goal, 3 and 7 Days in a Row, Star Catcher, Sticker Fan, Super Collector, plus v6's Learner (a lesson), Scholar (10 lessons) and Mistake Fixer (5 mistakes fixed for good).
- **Daily goal**: 3 rounds a day (the parent can change it), shown with a progress ring. There's also a 🔥 **days-in-a-row** counter. Both use the device's local date.

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

**4th grade**
- **Multiplication:** L1–2 2-digit × 1-digit → L3 hundreds × 1-digit → L4–5 3- and 4-digit × 1-digit → L6 × multiples of 10 → L7–8 2-digit × 2-digit (area model / partial products in the explanation) → L9 missing factor → L10 mixed
- **Long Division:** L1–2 facts and 2-digit ÷ 1-digit → L3–4 with remainders (tap "q R r") → L5 3-digit → L6 4-digit with remainder → L7–8 zeros in the quotient, 4-digit → L9 remainders → L10 "how many vans?" (round the answer up)
- **Fractions:** L1–2 equivalent fractions (picture, missing number) → L3 compare → L4–5 add/subtract like denominators → L6 improper → mixed number → L7 equivalent with bigger numbers → L8 add mixed numbers → L9 whole × fraction → L10 stories
- **Decimals:** L1–2 tenths/hundredths from a shaded grid → L3–4 fraction ↔ decimal → L5 compare → L6 digit places → L7 tenths + hundredths → L8 greatest decimal → L9 money as decimals → L10 0.70 = 0.7
- **Place Value & Rounding:** L1 digit values to 100,000s → L2 expanded form → L3 number names → L4–7 round to ten … hundred thousand → L8 compare 6-digit numbers → L9 10,000 more/less → L10 mixed
- **Factors & Primes:** multiples, factors, next multiple, prime or composite, number of factors, "not a factor", factor pairs, least common multiple
- **Angles & Measurement:** angle types (acute/right/obtuse/straight, tap) → feet/inches, hours/minutes, km/m, pounds/ounces → missing angle in a right or straight angle → adjacent angles → mixed units (6 lb 11 oz) → area in a story
- **Word Problems:** "times as many" (both ways) → equal groups → leftovers → two-step stories → buses needed (round up) → money → multi-step sharing

**5th grade**
- **Multiplication:** 2- and 3-digit × 1- and 2-digit → 4-digit × 2-digit → multiples of 10 → best estimate (tap) → missing factor
- **Division:** 3-digit ÷ 1-digit → ÷ multiples of 10 → 2-digit divisors, with and without remainders → estimate quotients (tap) → missing dividend → "cartons needed" stories
- **Fractions:** common denominators → add/subtract unlike denominators (answers as fractions or mixed numbers; any equivalent form accepted, e.g. 2/4 for 1/2) → mixed numbers → multiply fractions → division as a fraction (5 pizzas ÷ 8 friends) → stories
- **Decimal Operations:** add/subtract tenths and hundredths → decimal × whole → decimal × decimal → ÷ whole → ÷ decimal → rounding → money (answers accepted with or without trailing zeros: 2.50 = 2.5)
- **Powers of 10:** 10² … 10⁴, zeros in a power of 10, × and ÷ by 10/100/1,000 (moving the decimal point), missing power, × 10ⁿ
- **Order of Operations:** × before + → parentheses → ÷ → two operations with ( ) → brackets [ ] → four operations → match words to an expression (tap)
- **Volume:** count unit cubes in a picture → l × w × h → base area × height → missing edge → two-box shapes → cubes
- **Coordinate Plane (tap):** find the point at (x, y), read a point's coordinates, distance along a line, x-coordinate, patterns, the 4th corner of a rectangle, moving a point
- **Word Problems:** multi-digit × and ÷, money with decimals, fraction sums, change from $20, volume, "how many full boxes", fraction of a group, sharing a bill

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

v5 adds these keys and never changes the v4 ones:
- `mp_profile` {name, avatar}
- `mp_stars`, `mp_stars_total`, `mp_stickers` (array of ids), `mp_badges` {id: date}
- `mp_daily` {date, rounds, questions, done}, `mp_days` {last, count, best}
- `mp_btc_best_<grade>_<mode>` (Beat the Clock best)
- `mp_boss_wins`, `mp_rounds_total`, `mp_played` (modes tried), `mp_muted`

Existing v4 players keep all their levels and bests. They see the name/buddy screen once, get 3 welcome stars, and get any Level 10 Hero badge they already earned.

**v6 (profiles).** The first kid (profile `p1`) keeps using exactly the keys above. So all v1–v5 progress (name, buddy, levels, bests, stars, stickers, badges, streak, daily goal) simply *is* the first profile. Nothing is copied, renamed, or lost, and an older cached version would still see it. Other kids get the same keys with their id inside, e.g. `mp_p2_stars` or `mp_p2_level_4_mult`. New per-kid keys:
- `mp_settings` {goal, timer, grades, sound, readAloud, autoRead}
- `mp_stats` {secs, rounds, qs, correct, modes, days, types}
- `mp_mistakes` (saved questions with due date, wins, lapses)
- `mp_lessons`, `mp_fixed`

Device-wide keys: `mp_profiles` (list of kid ids), `mp_active`, `mp_parent` (PIN hash), `mp_migrated_v6`. On first v6 launch the dashboard's round count starts from the old `mp_rounds_total`. Time, accuracy and per-topic history start from v6.

## Adding a grade or mode

In `index.html`: write one generator per mode (`function genG6Something(level) { … return problem; }` for levels 1–10), add an entry to `GRADES` and its key to `GRADE_ORDER`, and add a lesson to `LESSONS` (`"6:something": function () { return [LS(title, html), …]; }`). The grade chip, tiles, saving, levels, scoring, review, and stats all come from the registry. A problem is an object like
`{ html, answer, displayAnswer, inputType: "number" | "text" | "choice" | "compare", choices?, key, hint?, steps? }` (helpers: `numQ`, `choiceQ`, `compareQ`, `decQ`, `fracQ`, plus the SVG helpers for clocks, coins, fractions, rulers, rectangles, angles, grids, cubes and the coordinate plane). If `hint`/`steps` are missing, `explainProblem()` builds them from the question.

## Files

```
index.html              app (HTML + CSS + JS, self-contained: generators, lessons, explanations, profiles, dashboard)
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


When you change any file, bump `CACHE_VERSION` in `service-worker.js` (currently `math-practice-v7`) so devices pick up the new version (it takes effect on the next launch after an online visit).

## Privacy (v7)

The app collects no data: no accounts, ads, analytics or tracking, and all progress stays in the device's local storage. The privacy policy is at [privacy.html](privacy.html) (https://kranthi-rigas.github.io/math-practice/privacy.html). It is also shown inside the app from the PIN-protected parent dashboard (**ℹ️ About & privacy**). The app itself contains no external links, so it meets the kids-category rules for the App Store and Google Play.

v7 also adds a `MathPractice.back()` hook. The Android app calls it for the system back button: it goes back one screen, and at the home screen it returns `false` so the app exits. The service worker is skipped inside the native (Capacitor) apps, because they already bundle every file. The native wrapper project is kept separately from this repo.
