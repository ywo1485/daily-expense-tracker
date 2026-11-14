# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Anyone who wants to build a habit of recording what they spend each day. It is a public product: people arrive by link, with no account, and should understand it and log a first expense without help. Most use is a quick visit on a phone, a few times a day.

## Product Purpose

Daily Spend records daily expenses in ringgit (RM) and makes the habit stick. Success is a person logging on the day itself, day after day, and being able to see where the month's money went.

## Positioning

The habit is carried by a pet panda. Logging on the day feeds it; missing days makes it hungry, then sad, then sleepy, and it never dies. The reward for consistency is a companion, not a chart.

## Operating Context

- Log an amount, pick a category, optionally add a note. A day with no spending can be logged as a no-spend day.
- Past days can be filled in from the calendar, but only logging on the day itself feeds the panda and counts toward the streak.
- A month view shows which days are logged; a monthly budget shows what is left and a per-day allowance.
- A month's entries can be downloaded as a CSV file.

## Capabilities and Constraints

- Single static page (`index.html`), no build step, no backend, deployed on Vercel.
- Data lives in the browser's `localStorage`: no account, no sync between devices.
- Currency is RM only.
- Must keep working as they do today: panda feeding, moods, tummy meter and keepsakes (flower at 3 days, scarf at 7, crown at 30); the monthly budget; CSV export. Badges, points and levels were removed at the owner's request.
- Categories can be added, renamed and removed in Settings (1 to 16). Entries of a removed category are kept and shown as Other.
- Undecided: multi-currency, accounts or sync, CSV import.

## Brand Commitments

- Name: Daily Spend. The panda's default name is Mochi and the user can rename it.
- The look is a pastel loyalty stamp card, recorded in DESIGN.md. It is always light: there is no dark theme.
- Voice: warm, short, plain. The panda speaks in first person.

## Evidence on Hand

No testimonials, user counts, press or pricing exist. Do not invent any.

## Product Principles

1. Logging takes seconds: amount, category, done.
2. Encourage, never punish. A missed day is an invitation back.
3. The panda is the reward; numbers support it.
4. A first-time visitor understands the page without instructions.
5. Private by default: the data stays on the person's device, and the page says so.
