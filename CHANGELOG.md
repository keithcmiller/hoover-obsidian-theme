# Changelog

All notable changes to the Hoover Obsidian Theme are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [1.1.1] — 2026-04-29

### Fixed
- Table headers now remain legible when printing or exporting to PDF.
  Previously, white text on a colored background became invisible when
  printers stripped background colors. Headers now use slate text on a
  cream background with a green underline, so they read on color and
  black-and-white printers alike.
- Dark mode notes now correctly force light-mode colors during print
  via `print-color-adjust` rules, so any printer engine respects them.
- Callouts now print with a visible border instead of relying on
  background tint that some printers strip.
- Division-scoped notes (`hoover-twp`, `hoover-has`) print with a
  neutral slate left border instead of orange or blue ink.

### Added
- Print stylesheet hides workspace chrome (status bar, ribbon, tab
  headers) so printed output contains only the note content.
- Links print in dark green underlined text rather than the on-screen
  accent color.

---

## [1.1.0] — 2026-04-26

### Added

#### Theme
- Personal callout (`> [!personal]`) using Hoover Violet (`#B565E5`)
- `--hoover-violet-rgb` token added to shared brand token layer
- Personal callout uses italic body-weight title to visually distinguish
  it from division callouts, which use N27 uppercase
- Soft violet fill at 7% opacity (light mode) and 10% (dark mode) —
  ambient rather than prominent, consistent with its non-work purpose
- Auto-label suffix "— Personal" appended to callout title

#### Templates
- `TPL — Daily Note.md` — daily anchor note with Focus, Top 3, Meetings
  & Conversations, Pipeline Quick Pulse, Ideas, and End of Day checklist
- `TPL — Weekly Review.md` — structured weekly close and forward-look,
  with division callout sections for TWP and HAS context
- `TPL — New Product Concept.md` — concept intake from problem statement
  through open questions and stage history log
- `TPL — Product Development Tracker.md` — stage gate progress, spec
  lock, workstream task tables, risk register, budget tracking, change
  log, and post-launch review
- `TPL — Meeting Notes.md` — agenda, decisions, and action items with
  inline guidance on writing trackable tasks using `#action` tags
- `TPL — Vendor Evaluation.md` — supplier profile with evaluation
  scoring, compliance tracking, interaction log, and recommendation

#### Vault infrastructure
- `Product Pipeline Master.md` — index note tracking all active, on-hold,
  and recently launched products across TWP and HAS, with vendor register
- `Task Dashboard.md` — pinnable Dataview-powered dashboard with six
  live query sections: overdue daily tasks, today's tasks, meeting
  actions, waiting-on items, product file tasks, and full-vault sweep
- `TEMPLATER_SETUP_GUIDE.md` — complete Templater setup walkthrough
  including folder templates, Daily Notes integration, naming conventions,
  daily/weekly habit structure, and quick reference card

#### Documentation
- `examples/hoover-parent-example.md` — fictional parent brand project
  note for screenshot and onboarding reference
- `examples/hoover-twp-example.md` — fictional Treated Wood Products
  specification note demonstrating TWP division styling
- `examples/hoover-has-example.md` — fictional Architectural Solutions
  cladding reference note demonstrating HAS division styling
- `SCREENSHOT_GUIDE.md` — step-by-step guide for taking screenshots and
  adding them to the repository README
- `GITHUB_GUIDE.md` — beginner-friendly guide covering account setup,
  GitHub Desktop, creating and cloning a repository, inviting colleagues,
  and the update/release workflow

### Changed
- `TPL — Daily Note.md` updated to include:
  - Dataview rollover block surfacing unchecked tasks from all previous
    daily notes automatically
  - Dataview block in Blocked / Waiting On filtering for `#waiting` tags
  - Inline expression pulling yesterday's Tomorrow's focus field into
    today's Focus section automatically
  - Expanded Meetings & Conversations comment explaining `#action` and
    `#waiting/person` tagging syntax for trackable meeting tasks
  - End of Day checklist updated to include action-tagging reminder

---

## [1.0.0] — 2026-04-24

### Added
- Initial theme release
- Light mode: Hoover Cream background (`#F0E9DD`), Hoover Slate text (`#283A40`)
- Dark mode: Hoover Slate background, Hoover Cream text
- Primary color palette: Hoover Green (`#31C576`), Slate, Cream
- Full secondary palette: Black (`#151F22`), Dark Green (`#1E7848`),
  Mint (`#C8DFCF`), White
- Full tertiary palette tokens: Red, Orange, Gold, Light Blue, Blue, Violet
- Division accent switching:
  - `hoover-twp` cssclass → Hoover Orange (`#FF6C13`) for Treated Wood Products
  - `hoover-has` cssclass → Hoover Blue (`#1BA0F5`) for Architectural Solutions
- Division callout blocks (`[!twp]`, `[!has]`) with auto-labels
- N27 headline font with Acumin Pro body, falling back to system sans-serif
- Heading color system: H2 = accent, H3 = dark green
- Branded table headers, blockquotes, horizontal rule, and code blocks
- Style Settings plugin support with division selector dropdown
- Per-note cssclasses support (`hoover-twp`, `hoover-has`)
- Print/PDF export fixes for dark mode
- `.hide-properties`, `.hoover-hdcl`, `.hoover-hi-line`,
  `.hoover-boxed-tags`, `.hoover-rm-status` class toggles
