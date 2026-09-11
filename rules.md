# Meal planning rules

These apply whenever a 5-day meal mix is generated from `meals.json` in this repo —
by either Ross or his wife, from any conversation with Claude.

## Variety rules
- **No repeated protein** across the 5 days (e.g. don't pick beef mince twice).
- **At least one meat-free night** in the 5.

## Week structure
- The week runs **Sunday through Thursday** (5 days) — the big grocery shop happens
  on the weekend and covers dinners through Thursday night. Friday and Saturday are
  not part of this rotation.

## Data format
`meals.json` is an array of recipe objects. Each has:
- `title`, `source` (link or cookbook/page), `notes`
- `protein`, `carbBase` — used to apply the variety rules above
- `ingredients` — full list, used to build a shopping list
- `status` (`idea` / `planned` / `cooked`), `day` (Sun/Mon/Tue/Wed/Thu or null)
- `rating` (1-5) and `feedback` — filled in once a meal's been cooked, to inform
  future picks (e.g. favour highly-rated meals, retire poorly-rated ones)

## Adding a recipe
Send a link, a cookbook photo, or just a name — whoever's chatting with Claude can
add to this repo the same way, no special process required.
