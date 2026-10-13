# Silvie — Product Brief

_Source: recorded planning conversation, Tuesday 2:26 PM (transcript via AudioToText.com). Living document._

## The problem

1. **Ideas drop like a rock.** A project gets discussed ("great idea!") and then is forgotten until it resurfaces by accident.
2. **Routine work is invisible.** A lot gets done but isn't documented, so nobody can see what anyone spends their time on.
3. **Unplanned work goes unrecorded.** People work the agreed list, then go off and do other things without telling each other.
4. **Stalled projects have no restart point.** Example: the inventory project has started but stalled. There's no record of where it stopped or how to pick it back up.
5. **Repeatable routines are forgotten.** "I did this really cool repeatable thing once but can't remember how."
6. **Feedback gets lost.** Requests made weeks ago fall through the cracks between collaborators.

## The proposal

A **mobile-first web app** (opened from a URL in Chrome, feels like a native phone app) that serves as the household's **single shared dashboard**:

- **One cloud source of truth.** Nothing saves to the phone; every user sees every change.
- **Built out over time.** Start with what looks good, and add sections as needs come up.
- **Clean and easy.** Paged sections and folders, swipeable, with buttons and toggles where they're relevant.
- **Powered by the Claude API**, so it acts intelligently instead of just doing mechanical data entry.
- **Beta URL** for the primary user to review the live build any time and give feedback.
- Target: **~2–3 weeks** of focused work for the first usable version.

## Users

| User | Access |
|---|---|
| Developer (son-in-law) | Full |
| Primary user (mother-in-law) | Full |
| Amara | Full (dashboard access) |
| Tenants | Limited: house rules, rent info |

## Features

### 1. Tasks & projects
- **Task → subtask** and **project → sub-project** hierarchy.
- **Categories** (an existing set already exists, e.g. *Gardening*).
- **Routine vs. project-based** items.
- **Top 12**: the current priority list, easy to identify at a glance.
- **Completion flow.** Finished items migrate out of current focus into an archive/backlog, and the follow-up item is surfaced.
- **Stalled status.** Records where a project stalled and how to resume it.

### 2. Horizon / planning tiers
Items can be toggled between:
- **Current**: on the active roster.
- **Watch**: future goals not on the current roster but kept in view.
- **Pie in the sky**: flagged as unrealistic right now.

Big projects get a **planning component**: who will do it, budget, funding source, and timeline.
_Example: new roof, needed within 1–2 years._

### 3. Activity log
- Records what was actually done, **including unplanned work**.
  _"I know it wasn't on the list, but I weeded the driveway for six hours."_
- Records payments. _"Paid Marta $120."_
- Makes routine, undocumented work visible.

### 4. Procedures (how-to library)
- Step-by-step instructions for repeatable routines.
- Claude helps draft and tighten them: concise, no repetition, ideas put where they logically belong.
- First procedure: **how to do the inventory**.

### 5. Inventory
- An image directory plus a spreadsheet of what each image is, with descriptions. The existing system is good and just needs to be followed and fleshed out.
- Browse images and **download them directly from the app**.

### 6. Meetings
Each meeting gets a structured agenda:
- What we hoped to accomplish
- What we did accomplish
- What still needs to be accomplished
- Future goals (watch list) and pie-in-the-sky items

### 7. Tenants
- **Tenant-facing view**: house rules, rent.
- **Tenant profiles** (internal): photo, about, notes.
- **Active roster**. When a tenant moves out, the profile goes **dormant** into a backlog but is kept.

### 8. Hidden Well section
- A dedicated "Hidden Well" portion of the app. _(Scope TBD.)_

### 9. Claude assistant bar (core feature)
Pinned at the **bottom of every screen**: a text field plus a **microphone button**.

- **Natural-language entry.** _"I took the trash out, paid Marta $120, and did some work on the pillars."_ Claude parses this, **confirms its understanding** ("So you did work on the pillars?"), and on confirmation files each item in the right place.
- **Accountability and reminders.** Claude proactively surfaces neglected items:
  _"We got really far on X, but we've been neglecting the gates. Want to check on that now?"_
- **Organizing raw input.** Concise, de-duplicated, logically grouped.

### 10. In-app feedback
- A place to submit ideas and feedback on the app itself, which go into the dev to-do list.

## Interim feedback process (until in-app feedback exists)

Use a shared live Google Doc (or text messages) in this format:

```
Idea one

Idea two

Idea three
______________________________ 2026-10-13
```

One idea per paragraph, separated by blank lines. Close each batch with a line of underscores and the date, so it's clear what's new and what's already been handled.

## Data sources to ingest
- Existing spreadsheet (currently standing in for a database) and its categories.
- Inventory images plus their description spreadsheet.
- Past chat logs, including the **Energy / House project** log (large and unwieldy). These need to be parsed down to their useful bits.

## Open questions
- [ ] **Backend / storage.** Keep a spreadsheet (Google Sheets) as the visible source of truth, or use a real database with spreadsheet export?
- [ ] **Auth.** How each user signs in. How tenant-limited access is enforced.
- [ ] **Hosting** for the app and beta URL.
- [ ] **Claude API key.** It must stay server-side and never ship to the browser.
- [ ] **Hidden Well** section: what it contains and who can see it.
- [ ] Where the existing spreadsheet, category list and inventory images live today.
- [ ] Voice input: browser speech-to-text vs. a transcription API.
