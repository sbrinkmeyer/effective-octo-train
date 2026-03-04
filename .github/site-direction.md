# Personal Site Direction (Non-Blog-First)

This plan is for a personal site that showcases work and hobbies without requiring frequent blogging.

## Positioning

- Goal: Present who you are, what you do, and what you care about.
- Constraint: Minimal ongoing maintenance.
- Not a goal: Selling products or posting high-volume thought content.

## Recommended Site Structure

1. Home (`/`)
   - Short intro (who you are + what you work on)
   - 2 tracks: "Work" and "Hobbies"
   - A clear contact action

2. Work (`/work/`)
   - 3–6 concise project summaries
   - For each: problem, what you did, impact, tools
   - Link to external artifacts (GitHub, docs, talks) when possible

3. Hobbies (`/hobbies/`)
   - Curated list of interests and a few examples per interest
   - Emphasize what you build/make/learn, not long narratives

4. About (`/about/`)
   - Personal background and values in a short format
   - Optional "Now" section (current focus)

5. Contact (`/contact/`)
   - Keep the existing page and make the call-to-action specific

## Content System (Low Effort)

Use these repeatable content formats:

- Work item card (4 bullets):
  - Context
  - Action
  - Result
  - Stack

- Hobby item card (3 bullets):
  - What it is
  - Why you enjoy it
  - One concrete example

This avoids blog pressure and still keeps the site fresh.

## 30-Day Starter Path

Week 1
- Publish home, work, and hobbies pages with placeholders.
- Add 2 work items and 2 hobby items.

Week 2
- Improve visual hierarchy and readability.
- Tighten nav labels and page intros.

Week 3
- Add 2–3 more work items.
- Add one short "Now" update (optional, not a blog post).

Week 4
- Review with UX + design checklist.
- Deploy cleanly and stop—only update when meaningful.

## What “Done Enough” Looks Like

- A visitor can answer in 30 seconds:
  - Who you are
  - What kind of work you do
  - What you enjoy outside work
  - How to contact you

If all four are clear, the site is already successful.

## Next Build Actions in This Repo

1. Add pages: `content/work.md`, `content/hobbies.md`, `content/about.md`
2. Update menu in `hugo.toml` to include Work and Hobbies
3. Keep posts optional; no pressure to publish regularly
4. Run local preview and do one Netlify-ready build check
