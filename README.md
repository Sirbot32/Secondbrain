# Secondbrain

This is an Obsidian vault, edited primarily through Claude Code using the `/deep-dive` skill (`.claude/skills/deep-dive/SKILL.md`). It can also be opened directly in Obsidian (desktop or mobile) like any other vault.

## Layout
- `Notes/` — atomic notes, one file per discrete concept or fact (Zettelkasten style). Flat pool, no subfolders — notes link to each other via `[[wikilinks]]` regardless of which topic surfaced them.
- `MOCs/` — one "Map of Content" file per broad topic (e.g. `MOCs/Stocks.md`), linking out to the atomic notes that belong to it.
- `Learning Queue.md` — persistent, checkbox-style list of things identified as unknown/uncertain, grouped by topic. Check items off as they're learned; don't delete them.
- `Books of Interest.md` — books matching topics shown genuine interest in, grouped by topic.
- `Books to Learn From.md` — books mapped directly to specific Learning Queue gaps, grouped by topic.

## Workflow
Run `/deep-dive <topic>` (e.g. `/deep-dive stocks`) to have a structured conversation that surfaces what you know and don't know about a topic. Confirmed knowledge becomes atomic notes + an updated MOC; gaps get appended to the Learning Queue. The skill commits and pushes to the current branch at the end of a session but never merges to `main` — that's done manually.

## Multi-device note
Claude Code web/cloud sessions work on auto-generated branches and push there; merge into `main` yourself once you're back on your own machine. Desktop Claude Code and Obsidian mobile/desktop apps (if used later) work directly against `main` via your own git clone/sync.
