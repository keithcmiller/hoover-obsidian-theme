# Hoover Obsidian Theme

An [Obsidian](https://obsidian.md) theme built to the **Hoover Brand Guidelines V2.0**, for use by Hoover employees and teams working across the parent brand and its divisions.

Supports both **light** and **dark** modes, and includes built-in styling for switching between the three brand identities. Ships with a complete vault template system for New Product Development workflows.

| Division | Accent Color |
|---|---|
| **Hoover** (parent) | Hoover Green `#31C576` |
| **Hoover Treated Wood Products** | Hoover Orange `#FF6C13` |
| **Hoover Architectural Solutions** | Hoover Blue `#1BA0F5` |

---

## Screenshots

> *(Add screenshots here — see [SCREENSHOT_GUIDE.md](SCREENSHOT_GUIDE.md))*

---

## Installation

### Manual (recommended for internal use)

1. In your Obsidian vault, open `.obsidian/themes/` (create it if it doesn't exist)
2. Inside `themes/`, create a new folder called `Hoover`
3. Copy `theme.css` and `manifest.json` into that folder
4. In Obsidian: **Settings → Appearance → Themes → Hoover**

```
YourVault/
└── .obsidian/
    └── themes/
        └── Hoover/
            ├── theme.css
            └── manifest.json
```

> **Note:** `.obsidian` is a hidden folder. On Windows, enable "Show hidden items" in File Explorer. On Mac, press `Cmd + Shift + .`

---

## Templates

The `templates/` folder contains a full workflow system for New Product Development. Copy the contents into your vault's `_Templates/` folder.

| Template | Purpose |
|---|---|
| `TPL — Daily Note.md` | Morning anchor with Dataview task rollover |
| `TPL — Weekly Review.md` | Weekly close and forward-look |
| `TPL — New Product Concept.md` | Concept intake through stage history |
| `TPL — Product Development Tracker.md` | Full gate-to-launch tracker |
| `TPL — Meeting Notes.md` | Agenda, decisions, trackable action items |
| `TPL — Vendor Evaluation.md` | Supplier profile and scoring |
| `Product Pipeline Master.md` | Live index of all products and vendors |
| `Task Dashboard.md` | Pinnable Dataview task view across the vault |

### Required plugins for templates

- **[Templater](https://github.com/SilverStreet/Templater)** — powers all date expressions and folder-based auto-templating
- **[Dataview](https://github.com/blacksmithgu/obsidian-dataview)** — powers the task rollover in daily notes and the Task Dashboard

See [TEMPLATER_SETUP_GUIDE.md](templates/TEMPLATER_SETUP_GUIDE.md) for complete setup instructions.

---

## Callouts

| Callout | Syntax | Color | Purpose |
|---|---|---|---|
| Note | `> [!note]` | Hoover Green | General information |
| Tip | `> [!tip]` | Dark Green | Recommendations |
| Warning | `> [!warning]` | Hoover Orange | Cautions |
| Danger | `> [!danger]` | Hoover Red | Critical alerts |
| Treated Wood Products | `> [!twp]` | Hoover Orange | TWP division context |
| Architectural Solutions | `> [!has]` | Hoover Blue | HAS division context |
| Personal | `> [!personal]` | Hoover Violet | Non-work items |

---

## Division Switching

### Per-note (frontmatter)

```yaml
---
cssclasses:
  - hoover-twp
---
```

| Class | Division |
|---|---|
| *(none)* | Hoover parent brand |
| `hoover-twp` | Hoover Treated Wood Products |
| `hoover-has` | Hoover Architectural Solutions |

### Per-section callout

```markdown
> [!twp]
> This section covers Treated Wood Products specifications.

> [!has]
> This section relates to an Architectural Solutions project.

> [!personal]
> Personal note — not for work context.
```

### Vault-wide (Style Settings plugin)

If your team uses the [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) plugin, a division selector dropdown is available under **Settings → Style Settings → Hoover Brand Theme**.

---

## Color Reference

| Name | Hex | Usage |
|---|---|---|
| Hoover Green | `#31C576` | Primary accent, links, active elements |
| Hoover Slate | `#283A40` | Primary text (light), dark backgrounds |
| Hoover Cream | `#F0E9DD` | Light mode background, dark mode text |
| Hoover Dark Green | `#1E7848` | H3 headings, hover states |
| Hoover Black | `#151F22` | Darkest background layer |
| Hoover Mint | `#C8DFCF` | Muted text (dark mode) |
| Hoover Orange | `#FF6C13` | Treated Wood Products accent |
| Hoover Blue | `#1BA0F5` | Architectural Solutions accent |
| Hoover Violet | `#B565E5` | Personal callout |

---

## Typography

| Role | Font |
|---|---|
| Headlines (H1–H6) | **N27 Medium** |
| Body copy | **Acumin Pro** (Light / Regular) |
| Labels / bold copy | **Acumin Pro** (Semibold / Bold) |
| Code | JetBrains Mono / Fira Code / system monospace |

Fonts must be installed on your system separately. Falls back cleanly to system sans-serif if unavailable.

---

## Repository Contents

```
hoover-obsidian-theme/
├── theme.css                   Core theme
├── manifest.json               Obsidian theme metadata
├── README.md                   This file
├── CHANGELOG.md                Version history
├── GITHUB_GUIDE.md             GitHub setup guide for beginners
├── SCREENSHOT_GUIDE.md         How to take and add screenshots
├── examples/                   Fictional example notes for screenshots
│   ├── hoover-parent-example.md
│   ├── hoover-twp-example.md
│   └── hoover-has-example.md
└── templates/                  Vault template system
    ├── TEMPLATER_SETUP_GUIDE.md
    ├── Product Pipeline Master.md
    ├── Task Dashboard.md
    ├── TPL — Daily Note.md
    ├── TPL — Weekly Review.md
    ├── TPL — New Product Concept.md
    ├── TPL — Product Development Tracker.md
    ├── TPL — Meeting Notes.md
    └── TPL — Vendor Evaluation.md
```

---

## Versioning

Follows [Semantic Versioning](https://semver.org/): `MAJOR.MINOR.PATCH`

See [CHANGELOG.md](CHANGELOG.md) for full history.

---

## License

Internal use only. This theme incorporates Hoover brand colors and typography per the Hoover Brand Guidelines V2.0. Do not distribute outside the organization.
