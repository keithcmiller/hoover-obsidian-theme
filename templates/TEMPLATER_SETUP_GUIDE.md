# Templater Setup & Daily Use Guide
## Hoover NPD Vault — Manager of New Product Development

This guide walks through setting up Templater, organizing your vault, and building
habits that will keep everything useful six months or two years from now.

---

## Part 1 — Initial Setup (do once)

### Step 1: Install Templater

If you haven't already:

1. In Obsidian, go to **Settings → Community plugins**
2. Turn off **Safe mode** if prompted
3. Click **Browse** and search for **Templater**
4. Click **Install**, then **Enable**

---

### Step 2: Create your vault folder structure

In your Obsidian vault, create the following folders. You can do this in the
file explorer panel on the left — right-click and choose **New folder**.

```
Your Vault/
├── 00 - Dashboard/
│   └── Product Pipeline Master.md    ← copy from the files provided
├── 01 - Daily Notes/
├── 02 - Weekly Reviews/
├── 03 - Products/
│   ├── TWP/
│   └── HAS/
├── 04 - Meetings/
├── 05 - Vendors/
├── 06 - Reference/
└── _Templates/                        ← put all TPL files here
```

> The underscore in `_Templates` keeps it sorted to the top or bottom of your
> file list so it stays out of the way.

---

### Step 3: Point Templater at your templates folder

1. Go to **Settings → Templater**
2. Find **Template folder location**
3. Type or select: `_Templates`
4. Enable **Trigger Templater on new file creation** — this is what makes
   templates run automatically when you create a note.

---

### Step 4: Set up folder templates (auto-template by location)

This is the most powerful Templater setting. It means: *when I create a note
in this folder, automatically use this template.*

Still in **Settings → Templater**, scroll to **Folder Templates** and click
**Add new folder template**. Set up each row:

| Folder | Template |
|---|---|
| `01 - Daily Notes` | `_Templates/TPL — Daily Note.md` |
| `02 - Weekly Reviews` | `_Templates/TPL — Weekly Review.md` |
| `03 - Products/TWP` | `_Templates/TPL — New Product Concept.md` |
| `03 - Products/HAS` | `_Templates/TPL — New Product Concept.md` |
| `04 - Meetings` | `_Templates/TPL — Meeting Notes.md` |
| `05 - Vendors` | `_Templates/TPL — Vendor Evaluation.md` |

After this, creating any note in those folders automatically drops in the
right template. You never have to remember which template to use.

---

### Step 5: Set up Daily Notes to use Templater

1. Go to **Settings → Daily Notes** (built-in Obsidian plugin — enable it
   if not already active)
2. Set **New file location** to `01 - Daily Notes`
3. Set **Date format** to `YYYY-MM-DD`
4. Leave **Template file location** blank — Templater's folder template
   will handle it automatically

Now pressing `Ctrl+Shift+D` (Windows) or `Cmd+Shift+D` (Mac) creates
today's daily note with the full template already filled in.

---

### Step 6: Place the Product Pipeline Master

Copy `Product Pipeline Master.md` into `00 - Dashboard/`. This is your
command center — pin it by right-clicking the file and choosing
**Pin to top** (or bookmark it in Obsidian's bookmark panel).

---

## Part 2 — The Templates Explained

---

### Daily Note (`TPL — Daily Note.md`)

**When:** Every working morning. Open it with `Ctrl+Shift+D` / `Cmd+Shift+D`.

**How to use it:**

- **Focus** — Write one sentence about what a successful day looks like.
  Not a to-do list. A picture of the day done well.
- **Top 3 Today** — Three tasks only. If you finish them, great. If you
  can't narrow it down to three, you haven't prioritized yet.
- **Product Pipeline — Quick Pulse** — Copy 2–4 rows from your Pipeline
  Master that need attention today. Don't duplicate data; just enough to
  keep those items in your peripheral vision.
- **Meetings & Conversations** — After each meeting, add one bullet:
  who, what was decided, what you own.
- **Ideas & Observations** — This section catches anything that doesn't
  fit elsewhere. Market signals, customer comments, friction you noticed.
  You'll mine this during weekly reviews.
- **End of Day** — Run through the checklist. The most important habit:
  *do not leave action items in the daily note.* Transfer them to the
  relevant product file before you close Obsidian.

**What it is not:** A meeting minutes document. A task manager. A journal.
Keep each section tight.

---

### Weekly Review (`TPL — Weekly Review.md`)

**When:** Friday afternoon or Monday morning. Block 30–45 minutes.
Create it in `02 - Weekly Reviews/` and name it `YYYY-WWW Weekly Review`
(e.g., `2026-W18 Weekly Review`).

**How to use it:**

- Start with **Last Week — Honest Look Back** before you look at next week.
  This is the most important habit in the system. It forces you to close
  the loop rather than always accelerating forward.
- **Product Pipeline — Weekly Snapshot** is a moment-in-time photo of
  pipeline health. After filling it in, go update the Pipeline Master too.
- **Division Notes** — Use the `[!twp]` and `[!has]` callouts to keep
  division context visible. Anything worth escalating or sharing with those
  teams should be noted here first.
- **Next Week's One Thing** — End with this. If the week can only
  accomplish one thing for the pipeline, what is it? This becomes the
  first item in next week's daily note Focus fields.

---

### New Product Concept (`TPL — New Product Concept.md`)

**When:** Any time a product idea is worth capturing — even rough ones.
Create it in `03 - Products/TWP/` or `03 - Products/HAS/` and name it
after the product or concept (e.g., `UC4B Composite Post System`).

**How to use it:**

- Fill in **The Problem** first. If you can't state the problem clearly,
  the concept isn't ready to be a file yet — put it in your daily note's
  Ideas section and let it sit.
- **Open Questions** is the most important section. Every concept has
  things you don't know. Writing them down forces clarity and creates
  a built-in next-action list.
- **Stage History** — Update this every time the product moves to a new
  stage. This becomes your audit trail.
- When a concept gets formal approval, promote it: create a new
  **Product Development Tracker** file for it and link the two together.

---

### Product Development Tracker (`TPL — Product Development Tracker.md`)

**When:** When a concept clears the first gate and moves into active
development. Name it the same as the concept file for easy linking.

**How to use it:**

- **Status Board** — Keep the Health field current. 🟢 / 🟡 / 🔴 / ⬜.
  If it's been 🟡 for more than two weeks without movement, something is
  wrong and needs a conversation.
- **Stage Gate Progress** — Check off gates as they're passed. Date them.
  This is your accountability record.
- **Change Log** — *Never change the Specifications table without adding
  a row to the Change Log.* This protects you when someone asks why
  a spec changed three months ago.
- **Launch Checklist** — Start filling this in 8 weeks before target
  launch. Don't wait until the week before.
- **Post-Launch Review** — The section most people skip. Don't. It's
  the most valuable thing you'll write for your own development as a
  product manager.

---

### Meeting Notes (`TPL — Meeting Notes.md`)

**When:** Before or at the start of any meeting worth documenting.
Create it in `04 - Meetings/` and name it `YYYY-MM-DD — Meeting Name`
(e.g., `2026-04-28 — TWP Contractor Feedback Call`).

**How to use it:**

- Fill in **Agenda** before the meeting starts.
- During the meeting, take notes under **Discussion Notes** — don't
  try to capture everything, just what matters.
- **Decisions Made** — Only actual decisions go here. "We discussed X"
  is not a decision.
- After the meeting: **immediately** transfer Action Items to the
  relevant product file or your daily note. The meeting file is an
  archive, not a working document.

---

### Vendor Evaluation (`TPL — Vendor Evaluation.md`)

**When:** Any time a supplier comes onto your radar as worth tracking.
Create it in `05 - Vendors/` and name it after the company.

**How to use it:**

- **Interaction Log** — Update this every time you speak with them,
  receive samples, or review their documentation. It becomes a
  relationship history that's invaluable when a question comes up
  months later.
- **Red Flags / Concerns** — Write concerns here the moment you notice
  them. It's easy to rationalize them away; writing them down keeps
  them honest.
- Add approved vendors to the **Approved Vendor Register** table in
  the Pipeline Master.

---

## Part 3 — The Daily Habit (the system only works if you use it)

### Morning (5–10 minutes)

1. `Ctrl+Shift+D` / `Cmd+Shift+D` — open today's daily note
2. Write your Focus sentence
3. Set your Top 3
4. Scan the Pipeline Master — anything urgent?

### During the day

- Log meetings in `04 - Meetings/` as they happen
- Transfer action items immediately — don't leave them in meeting files
- Add ideas to the daily note's Ideas section as they come up

### End of day (5 minutes)

- Run through the End of Day checklist in the daily note
- Transfer any open actions to relevant product files
- Set tomorrow's Top 3 if you can

### Friday (30–45 minutes)

- Create the weekly review in `02 - Weekly Reviews/`
- Update the Pipeline Master
- Update any product files whose stage or health changed

---

## Part 4 — Naming Conventions

Consistent naming makes linking and searching work well.

| File Type | Convention | Example |
|---|---|---|
| Daily note | `YYYY-MM-DD` | `2026-04-28` |
| Weekly review | `YYYY-WWW Weekly Review` | `2026-W18 Weekly Review` |
| Product concept | Descriptive product name | `UC4B Composite Post System` |
| Development tracker | Same as concept file + ` — Tracker` | `UC4B Composite Post System — Tracker` |
| Meeting | `YYYY-MM-DD — Description` | `2026-04-28 — TWP Contractor Feedback Call` |
| Vendor | Company name | `Acme Lumber Supply` |

---

## Part 5 — Inserting a Template Manually

Sometimes you'll want to apply a template to a note you've already created,
or choose a different template than the folder default.

1. Open the note
2. Press `Alt+E` (Windows) or `Option+E` (Mac) — this opens the Templater menu
3. Select **Insert Template**
4. Choose the template you want

You can also set this to a hotkey of your choice under
**Settings → Hotkeys → search "Templater"**.

---

## Quick Reference Card

| What I want to do | How |
|---|---|
| Open today's daily note | `Ctrl+Shift+D` / `Cmd+Shift+D` |
| Create a new product concept | New file in `03 - Products/TWP/` or `/HAS/` |
| Log a meeting | New file in `04 - Meetings/` |
| Add a vendor | New file in `05 - Vendors/` |
| Insert a template manually | `Alt+E` / `Option+E` |
| See the full pipeline | Open `00 - Dashboard/Product Pipeline Master` |
| Apply TWP division styling | Add `cssclasses: [hoover-twp]` to frontmatter |
| Apply HAS division styling | Add `cssclasses: [hoover-has]` to frontmatter |
| Mark a section as TWP context | `> [!twp]` callout |
| Mark a section as HAS context | `> [!has]` callout |
