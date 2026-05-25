---
type: daily
date: {{date:YYYY-MM-DD}}
tags: []
---
# {{date:dddd, MMMM D, YYYY}}

---

## Tasks due today
```dataview
TABLE priority, project AS "Project"
FROM "4 Tasks" OR "3 Projects"
WHERE type = "task" AND due >= date(this.date) AND due < date(this.date) + dur(1 day) AND status != "done" AND status != "cancelled"
SORT due ASC, priority ASC
```

---

## Notes

- 

## Journal


