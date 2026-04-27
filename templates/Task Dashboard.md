---
tags:
  - dashboard
---

# Task Dashboard

*Live view — everything open across your vault. Nothing lives here permanently. Check tasks off in their source files.*

---

## 🔴 Overdue — Daily Notes

Tasks from daily notes older than today that are still open.

```dataview
TASK
FROM "01 - Daily Notes"
WHERE !completed
AND file.name != dateformat(date(today), "yyyy-MM-dd")
SORT file.mtime ASC
```

---

## 🟡 Today's Open Tasks

```dataview
TASK
FROM "01 - Daily Notes"
WHERE !completed
AND file.name = dateformat(date(today), "yyyy-MM-dd")
```

---

## 🟠 Actions from Meetings

Tasks tagged `#action` across all meeting notes — open only.

```dataview
TASK
FROM "04 - Meetings"
WHERE !completed
SORT file.mtime DESC
```

---

## 🔵 Waiting On Someone

Tasks tagged `#waiting` anywhere in the vault.

```dataview
TASK
FROM "01 - Daily Notes" OR "04 - Meetings"
WHERE !completed
AND contains(tags, "waiting")
SORT file.mtime DESC
```

---

## ⬜ Open Product Actions

Tasks inside active product files — things you've flagged as next actions.

```dataview
TASK
FROM "03 - Products"
WHERE !completed
SORT file.mtime DESC
```

---

## All Open Tasks — Full Vault

Everything unchecked, everywhere, sorted by file age (oldest first so nothing gets buried).

```dataview
TASK
FROM "01 - Daily Notes" OR "03 - Products" OR "04 - Meetings" OR "05 - Vendors"
WHERE !completed
SORT file.mtime ASC
```

---

*Check tasks off in their source file — this dashboard updates instantly.*
