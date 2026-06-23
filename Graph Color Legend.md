---
tags: [meta]
created: 2026-06-23
---

# Graph Color Legend

Reference for the colors configured in `.obsidian/graph.json`. Node size in the graph scales with number of connections (links in + out); color is keyed off each note's `topic:` frontmatter property.

| Topic | Color |
|---|---|
| English | 🔴 Red |
| Math | 🔵 Blue |
| Biology | 🟢 Green |
| Chemistry | 🟢 Teal-green (science) |
| History | 🟡 Yellow |
| Computer Science | 🩵 Cyan (Math + Science) |
| AI | Teal (Math + Science) |
| Logic | Blue-violet (Math-adjacent reasoning) |
| Philosophy | 🟣 Purple (Humanities + reasoning) |
| Psychology | Lime (Science + Humanities) |
| Economics | 🟠 Orange (Humanities/History + Math) |

When adding a new subject, pick a color that blends its closest base subjects (English=red, Math=blue, Science=green, History=yellow) and add a matching `colorGroups` entry in `.obsidian/graph.json` keyed on `["topic":"<Subject>"]`.
