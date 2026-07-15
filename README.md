# CCGL Cultivation Schedule

Live production-schedule dashboard for the cultivation team. Enter 4 dates per cycle
(Clone Cut → Transplant to Rack → Transplant to Room → Flower Day 1) and the full
schedule auto-builds — defoles, harvest window, FF + dry harvest, room flip, and the
dry-room hang/bins timeline. Conflicts are flagged, never auto-moved.

## Files
- `index.html` — the whole app (single file)
- `state.json` — the live database (cycles, clone orders, strains, settings)

## Deploy (same flow as the inventory dashboard)
1. Create a new GitHub repo: `dangillan1/ccgl-cultivation` (public)
2. Upload `index.html` and `state.json` to the repo root, branch `main`
3. Repo Settings → Pages → Deploy from branch → `main` / root
4. App goes live at `https://dangillan1.github.io/ccgl-cultivation/`

## Logins (change in Settings → Access, then Publish)
| Who   | Password | Role      |
|-------|----------|-----------|
| Dan   | dabs     | editor    |
| Matt  | veg      | editor    |
| David | flower   | editor    |
| Guest | growlab  | view only |

## Publishing changes
Editors hit **Publish** — first time it asks for a GitHub personal access token
(fine-grained, Contents read/write on the ccgl-cultivation repo only). The token is
stored only in that browser. Edits are kept as a local draft until published.

## How dates auto-build (all tunable in Settings)
- Veg lengths = whatever your 4 input dates imply
- Flower runs to day 65, harvest-ready window shaded from day 56
- Defole 1 at flower day 21, Defole 2 at day 42 — 4-day passes, override per cycle
- FF harvest 2 days, then dry harvest 2 days (planned at flower day 63)
- Room flip 4 days after harvest
- Dry room: 14 days hanging → 14 days in bins
- Clone orders: slots × clones/slot + 70% overage (F1/F2: 12×90→153 cut; F3 scaled to 77/118 lights)

## Notes from the import (July 15, 2026)
- F1H09 + F2H10 imported as the active cycles; F1H10 drafted from the sheet (cut 8/13, room 9/10, flower 9/11)
- F2H10 transplant-to-room / flower day 1 estimated at 7/25 — confirm in the app
- Older cycles are archived under History (dates partly estimated)
- The Google Sheet stays alive for daily tasks / IPM / holidays — this app owns cycle planning
