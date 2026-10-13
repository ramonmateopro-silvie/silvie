# Working Order — Silvie

_The system of record. If it isn't written here, it isn't remembered. Update it in the same commit as the change._

## Current state (2026-10-13)
- Repo contains docs only: `CLAUDE.md`, `docs/PRODUCT_BRIEF.md`, this file. No app code yet.
- Inheritance doc received (older copy dated 2026-09-02; an updated version is being prepared).

## Rulings (settled; don't re-offer)
| Date | Ruling |
|---|---|
| 2026-10-13 | Real database, with spreadsheet export as an easy, highly visible feature for Anna. |
| 2026-10-13 | Hosting on Vercel. Per-user username + password; roles are full or tenant. |
| 2026-10-13 | Tenant app: same look, fewer pages (announcements, info & resources, limited feedback/contact). Exact pages decided after review. |
| 2026-10-13 | Hidden Well is its own app (repo `hiddenwell`); this app only gets a launch button. |
| 2026-10-13 | Anna's existing data is on her computer; Ramon hands it over at import time. |

## Tiered plan (proposed; awaiting Ramon's confirmation)
- **Tier 0 — Foundation** _(A SESSION)_: Next.js app scaffold, mobile/PWA shell, login + roles, database schema, visible BUILD_ID, gates, Vercel deploy flow.
- **Tier 1 — Core tracking** _(A SESSION–OVERNIGHT)_: tasks/subtasks, projects/sub-projects, categories, routine vs. project, Top 12, horizon tiers (current / watch / pie-in-the-sky), completion archive, stalled status + resume notes, big-project planning fields; activity log; **spreadsheet export button**.
- **Tier 2 — Claude bar** _(A SESSION)_: text + mic input, parse → confirm → file; neglect reminders.
- **Tier 3 — Knowledge** _(A SESSION)_: procedures library, inventory (images + descriptions + download), meetings.
- **Tier 4 — People** _(A SESSION)_: tenant app, tenant profiles (active/dormant), Hidden Well launch button, in-app feedback.
- **Tier 5 — Import** _(SMALL–A SESSION, depends on data)_: Anna's spreadsheet, categories, inventory images, chat logs.

## Open items / blocked on Ramon
- [ ] Confirm tier ordering above.
- [ ] Repo visibility: currently **public**. Recommend private before app code and the inheritance doc go in.
- [ ] Accounts: Vercel project, database provider (recommend Neon Postgres via Vercel), Vercel Blob for images, Claude API key. All are Ramon's accounts/spend.
- [ ] Deploy ref: which branch Vercel deploys from.
- [ ] Hidden Well launch URL / deep link.
- [ ] Updated inheritance doc.

## Interim feedback format
One idea per paragraph, blank lines between, each batch closed with a line of underscores and the date.
