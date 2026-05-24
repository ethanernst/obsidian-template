---
type: project
status: planning
priority: medium
due:
created: {{date:YYYY-MM-DD}}
source:
tags: []
---

## Overview

## Goals

-

## Tasks

```base
filters:
  and:
    - file.inFolder("3 Projects/{{VALUE:Project Name}}")
    - type == "task"
properties:
  file.name:
    displayName: Name
views:
  - type: table
    name: Project Tasks
    groupBy:
      property: status
      direction: ASC
    order:
      - file.name
      - priority
      - due
    columnSize:
      file.name: 255
      note.priority: 174
```

## Notes
