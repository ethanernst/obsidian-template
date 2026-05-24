[[1 Journal|Journal]] · [[3 Projects|Projects]] · [[4 Tasks|Tasks]] · [[5 Ideas|Ideas]] · [[2 Docs|Docs]] · [[6 Notes|Notes]]

---

## In Progress
```dataview
TABLE due, project AS "Project"
FROM "4 Tasks" OR "3 Projects"
WHERE type = "task" AND status = "in-progress"
SORT due ASC
```

## Due Soon
```dataview
TABLE due, status AS "Status", project AS "Project"
FROM "4 Tasks" OR "3 Projects"
WHERE type = "task" AND status != "done" AND status != "cancelled" AND due != null
SORT due ASC
LIMIT 8
```

## Recent Notes
```dataview
LIST
FROM "6 Notes" OR "2 Docs"
SORT file.mtime DESC
LIMIT 6
```
