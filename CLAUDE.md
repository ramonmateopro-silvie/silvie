# Silvie — read this first

Household dashboard app for Anna (Ramon's mother-in-law). Mobile-first web app on Vercel, shared cloud database, Claude-powered assistant bar.

## Read path (every session, in this order)
1. **Inheritance doc**: how to work with Ramon (communication, gates, deploy discipline, cost warnings). Ramon hands it over at the start of each session; it is deliberately **not committed** while this repo is public. If you don't have it, ask for it before building.
2. `docs/WORKING_ORDER.md`: current state, tiered plan, open items, rulings, and what's blocked on whom.
3. `docs/PRODUCT_BRIEF.md`: what the app is and why (from the original planning conversation).

## Standing rules (short form; the inheritance doc is canonical)
- Before any task, state its cost: **SMALL / A SESSION / OVERNIGHT**.
- Write rulings, requests and promised work into `docs/WORKING_ORDER.md` **in the same turn**, and commit.
- Docs ship in the same commit as the code they describe.
- Run the gates before every ship. Break a guard on purpose before trusting it.
- Never fail silently: always degrade to something visible.
- Bump the visible BUILD_ID on every ship.
- No backticks in `git commit -m` messages. No model identifiers in repo artifacts.
- Personal data (names, tenants, money, photos) lives in the database, never in the repo.
