---
tags:
  - daily-note
date: <% tp.date.now("YYYY-MM-DD") %>
week: "<% tp.date.now("YYYY-[W]WW") %>"
---

# <% tp.date.now("dddd, MMMM D, YYYY") %>

## Focus

*What does a successful day look like today? One or two sentences.*

**Carried from yesterday:** `= [[<% tp.date.now("YYYY-MM-DD", -1) %>]].tomorrow-focus`

---

## Rolled Over — Unfinished from Previous Days

> [!warning]
> These tasks are still open in your daily notes. Check them off there when done — they will disappear from this list automatically.

```dataview
TASK
FROM "01 - Daily Notes"
WHERE !completed
AND file.name != this.file.name
SORT file.mtime DESC
```

---

## Schedule

| Time | Block | Notes |
|---|---|---|
| Morning | | |
| Midday | | |
| Afternoon | | |

---

## Top 3 Today

- [ ] 
- [ ] 
- [ ] 

---

## In Progress

> [!note]
> Pull from your open product files and active projects. Update status there, not here.

- 
- 
- 

---

## Meetings & Conversations

<!--
HOW TO CREATE A TRACKABLE TASK FROM A MEETING:
  Write the action as a checkbox under the meeting bullet, tagged with #action
  and the person it involves. Example:

  - Met with Sarah (Ops) re: UC4B sourcing timeline
    - [ ] #action Follow up with Sarah on lead time quote by Friday #waiting/sarah
    - [ ] #action Send Sarah the spec sheet for UC4B-8 post

  The tag #action makes these queryable by Dataview anywhere in your vault.
  The #waiting/person tag lets you filter by who is blocking you.
  Tasks checked off here disappear from all rollover queries automatically.
-->

- 

---

## Product Pipeline — Quick Pulse

| Product / Initiative | Division | Stage | Next Action |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

---

## Decisions Made

*Any decisions you made or were part of today. Brief and factual.*

- 

---

## Blocked / Waiting On

```dataview
TASK
FROM "01 - Daily Notes"
WHERE !completed
AND contains(tags, "waiting")
AND file.name != this.file.name
SORT file.mtime DESC
```

---

## Ideas & Observations

*Anything worth capturing — market observations, customer comments, process friction, sparks of thought.*

- 

---

## End of Day

- [ ] Inbox cleared or triaged
- [ ] Open product files updated with any new actions from today
- [ ] Any #action tasks from meetings written as checkboxes above
- [ ] Tomorrow's focus written below
- [ ] Notes filed, not left here

**Tomorrow's focus:**
<% tp.frontmatter["tomorrow-focus"] ?? "" %>

---

## Related

- [[<% tp.date.now("YYYY-MM-DD", -1) %>]] ← Yesterday
- [[<% tp.date.now("YYYY-MM-DD", 1) %>]] → Tomorrow
- [[Weekly Review — <% tp.date.now("YYYY-[W]WW") %>]]
