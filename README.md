# Puy du Fou 3-Day Visit Planner

A single-file, offline-capable planner for a 3-day Puy du Fou visit. Pick show times, set a queue
buffer per show, get automatic conflict detection across the day, and a proportional visual agenda
of the whole day. Picks are saved per-day and cross-referenced so later days flag shows you've
already scheduled/seen. No backend — everything runs client-side and state is kept in the
browser's local storage.

Open `index.html` directly in a browser, or host it as a static site (see below).

## Data source

Show times are pulled directly from Puy du Fou's official "Programme for the day" page
(https://www.puydufou.com/france/en/program-for-the-day), read from the page's own
`TimeScheduler.CachedScheduleResult` data rather than estimated from the schedule graphic.
Puy du Fou only publishes each day's schedule about 2 days in advance, so days further out will
show as "not published yet" until re-scraped closer to the date.

Note: local storage is scoped per-origin, so picks made on one hosted URL won't follow you to a
different URL or device. Use the in-app "Export configuration" / "Import saved configuration"
buttons to carry a plan between them.
