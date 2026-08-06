# 2-Week Meal Planner

A single-file web app for planning two weeks of low-carb, Filipino-friendly meals. Pick a dish for every meal slot, tick meals off as you eat them, and print or save the result as a PDF.

**Live site:** https://gilbertconsebido-tacreg8.github.io/2weekmealplan/

## What it does

The app turns a static 14-day meal plan into something usable day to day. Instead of reading a fixed list, you choose each meal from a dropdown of plan-approved options, add your own dishes when you find one you like, tick meals off through the week, and keep a printable copy.

- **14 day cards**, each with breakfast, lunch, dinner, and an optional snack
- **Every slot is a dropdown** — swap any day's meal for any other option in that category
- **Check meals off** as you eat them; a day highlights when breakfast, lunch, and dinner are all done
- **Progress bar** counting completed main meals out of 42
- **Add food tab** — type in your own dish and it appears in every day's dropdown for that meal
- **Week filter** — view all 14 days, just Week 1, or just Week 2
- **Print / Save PDF** — flattens the dropdowns to plain text, expands the reference sections, and lays out two columns per page
- **Reference sections** — ground rules, fruit allowance, snack ideas, a weekly shopping list, and notes on prep, eating out, alcohol, and tracking progress
- **Light and dark** — follows your operating system setting

## The plan

A general low-carb, high-protein approach built around roughly 2,000–2,200 kcal a day, 180–190 g protein, 75–100 g net carbs, 120–140 g fat, and 3–4 litres of water. Carbohydrate is concentrated at breakfast so lunch and dinner stay light — no rice at those meals, just cauliflower rice, extra vegetables, or a larger portion of protein.

These figures are shown as reference chips in the header. The app does not calculate or enforce them.

## Running it

Open `index.html` in any browser. That's the whole thing — no install, no build step, no server.

It also works offline and straight from disk, because there are no network requests at all: no frameworks, no CDN, no web fonts, no analytics. The favicon is an inline SVG data URI.

## Note on saving

The app deliberately uses no browser storage, so your picks, check-marks, and any dishes you added reset when the page reloads. This keeps the file portable and self-contained. The intended way to keep a plan is **Print / Save PDF**.

To make a favourite dish permanent, add it to the `BASE_MEALS` arrays near the top of the `<script>` block in `index.html` and it ships as a built-in option.

## Built with

Plain HTML, CSS, and vanilla JavaScript in one file. CSS custom properties drive theming, with a `prefers-color-scheme` media query for the dark palette. Each day's selection is stored as the meal's text rather than an index, so adding or removing dishes never corrupts an existing pick — if a dish is removed, any day using it falls back to a valid option.

## Disclaimer

This app supports meal planning and is not medical advice. Anyone on regular medication or with recently flagged bloodwork should consult their doctor before a significant dietary change.
