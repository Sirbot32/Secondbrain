---
name: deep-dive
description: Conduct a structured knowledge-capture interview about a broad topic the user brings up (e.g. "stocks", "linear algebra"), surface what they already know vs. don't know, and write the results into this Obsidian vault as atomic notes plus a Learning Queue entry, committed to git. Use this whenever the user wants to "deep dive", "do a knowledge dump", explicitly invokes /deep-dive <topic>, or says things like "let's go through what I know about X" or "help me figure out my gaps in X."
---

# Deep Dive: Knowledge Capture Interview

This skill runs a structured interview to find out what the user actually knows about a topic, write the confirmed parts into this vault as atomic notes, and record the gaps separately so they're not lost. The point isn't to teach the user the topic — it's to get what's already in their head onto paper (accurately), and to make the holes visible and trackable.

## Step 1 — Identify the topic and load existing context

The user will name a broad topic (e.g. "stocks"). Before asking anything:

1. Check whether `MOCs/<Topic>.md` already exists. If it does, read it — this is a continuation of a previous session, not a fresh start. Skim the atomic notes it links to (just the titles, no need to open every one) so you don't re-ask about things already captured.
2. Check `Learning Queue.md` for an existing `## <Topic>` section and note what's already listed as a gap, so you don't re-surface the same gap as if it were new.
3. If neither exists, this is a brand-new topic — there's no setup needed beyond proceeding to Step 2.

## Step 2 — Run the interview

The goal is to get the user talking in their own words first, then probe. Don't lecture and don't fact-check against external sources mid-conversation — this is about capturing and clarifying *their* mental model, not grading it against a textbook.

1. **Open with a brain-dump prompt.** Ask the user to explain the topic as if to a smart friend who knows nothing about it — in their own words, no particular order, whatever comes to mind first. Let them talk before you ask anything pointed.
2. **Follow up on specifics.** For each distinct claim or concept the user raises, ask one focused follow-up that either (a) deepens it — "why does that happen" / "how does that actually work mechanically" — or (b) tests the edges — "does that always hold, or are there cases where it doesn't." Take these one at a time, not as a barrage.
3. **Explicitly surface uncertainty.** Watch for hedge language ("I think", "something like", "I'm not totally sure but"), and when the user pauses or struggles on something, ask directly: "Are you confident about that, or is that a guess?" Don't let an uncertain claim slide into being recorded as confirmed knowledge.
4. **Actively probe for unknown unknowns.** Beyond what the user volunteers, ask 2-4 questions a knowledgeable person in this domain would consider basic but the user hasn't brought up. The goal is finding gaps the user wouldn't have thought to mention, not exhaustively quizzing them.
5. **Keep a running mental tally** as the conversation proceeds of two buckets: (a) things the user stated clearly and confidently — these become atomic notes, and (b) things the user was unsure about, got wrong, or drew a blank on — these become Learning Queue entries. You don't need to announce this tally to the user mid-conversation; just track it so Step 3 and Step 4 go smoothly.

Keep the interview conversational and bounded — a handful of exchanges per session, not an exhaustive interrogation. When the user signals they're done (explicitly, or the conversation has naturally wound down), move to writing.

## Step 3 — Write or update the MOC

Before writing any atomic notes, create or update `MOCs/<Topic>.md` (Title Case topic name as filename).

If it doesn't exist, create it with this structure:

```markdown
---
tags: [moc]
topic: <Topic>
created: <YYYY-MM-DD>
---

# <Topic>

## Notes
- [[Concept Name]]
- [[Another Concept]]
```

If it already exists, just append new `- [[Concept Name]]` lines under `## Notes` for any newly-created atomic notes from this session — don't touch the frontmatter `created` date, and don't restructure what's already there.

## Step 4 — Write the atomic notes

For every item in the "confirmed knowledge" bucket from Step 2, create one atomic note per discrete concept or fact in `Notes/`. One file per idea — if the user explained three related-but-separable things, that's three files, not one.

Before creating a file, check whether `Notes/<Concept Name>.md` already exists (list `Notes/` or search for the exact filename):
- If it exists and is the same concept, don't duplicate it — instead, edit it to fold in any new detail from this conversation, and just link to it from the MOC (Step 3) if not already linked.
- If it exists but is a different concept that happens to share a name, name the new file `<Concept Name> (<disambiguator>).md` and briefly mention this to the user.

New atomic note structure:

```markdown
---
tags: [<topic-lowercase>]
topic: <Topic>
created: <YYYY-MM-DD>
status: confirmed
---

# <Concept Name>

<1-3 sentences capturing the concept in the user's own words/understanding, cleaned up for clarity but not rewritten into a textbook voice — this should still sound like what they actually told you.>

Related: [[Other Concept]], [[Another Related Concept]]
```

The `Related:` line is optional — only include it when there's a genuine link to another atomic note (existing or newly created this session). Don't force links that aren't real connections, and don't link to the MOC from the atomic note (the relationship is already captured by the MOC linking out to the note — keep it one-directional to avoid clutter).

Write notes in the user's own phrasing wherever possible. The point is capturing what they actually understand, not producing polished reference material.

## Step 5 — Append gaps to the Learning Queue

Open `Learning Queue.md` (create it at the vault root with the header below if it doesn't exist yet):

```markdown
# Learning Queue

Persistent list of things I've identified I don't know or am unsure about. Check items off (change `[ ]` to `[x]`) once learned — don't delete them, so there's a record.
```

For the "gaps" bucket from Step 2:
1. Check whether a `## <Topic>` section already exists in the file. If yes, append new bullets at the end of that section. If no, add a new `## <Topic>` section (alphabetical placement isn't necessary — append at the end of the file is fine).
2. Before adding each gap, skim the existing bullets (checked and unchecked) under that topic's section and skip anything that's substantively the same gap already listed.
3. Phrase each gap as a concrete, specific thing to learn, not a vague topic — bad: "options"; good: "How options pricing (Black-Scholes basics) actually works." Specific phrasing is what makes the queue actually actionable later, rather than a list of topic names the user will have to re-derive context for.

## Step 6 — Update the book lists

Maintain two standing root-level notes, both living documents updated incrementally across sessions (same pattern as `Learning Queue.md`):

- `Books of Interest.md` — books matching topics the user showed genuine interest in this session, regardless of whether the topic landed as confirmed knowledge or a gap. Append under a `## <Topic>` header (reuse it if it already exists).
- `Books to Learn From.md` — books that map directly to specific entries just added to `Learning Queue.md` this session. Not every gap needs a book — skip it if you don't have a confident, real recommendation. Don't force a 1:1 mapping just to fill space.

Rules for both:
1. Only recommend books you're confident actually exist with the title/author as stated. If you're not sure of exact bibliographic details, verify with WebSearch before writing it into the vault — a hallucinated title/author in a permanent reference note defeats the purpose.
2. Same structure as `Learning Queue.md`: no frontmatter, `## <Topic>` headers, one bullet per book formatted as `*Title* — Author. <one-line note on why it's relevant>`.
3. Create the file at the vault root with just the one-line header description (see existing files for the exact wording) if it doesn't exist yet.
4. Skip a book if it's already listed under that topic's section in the relevant file.

## Step 7 — Commit and push (no auto-merge)

Once the MOC, atomic notes, Learning Queue, and book lists are updated:

1. `git add` exactly the files changed or created this session (the MOC, the new/edited atomic notes, `Learning Queue.md`, `Books of Interest.md`, `Books to Learn From.md` — whichever actually changed) — avoid a blanket `git add -A` so nothing unrelated gets swept in.
2. Commit with a message summarizing the session, e.g. `Deep dive: Stocks — add 6 notes, 3 learning gaps`. Keep it one line; no need for a body.
3. Push to the **current branch** (`git push`, or `git push -u origin <branch>` if the branch has no upstream yet — check with `git status` first). Never merge, rebase onto, or push to `main`/`master` — the user explicitly merges these themselves later. If `git push` fails because there's no upstream tracking branch, set it with `-u` rather than trying to push to a different branch.
4. Tell the user what was committed and pushed (file count, branch name) so they know it's safely captured, and remind them it's on their working branch awaiting their manual merge into `main` — don't imply this has reached `main`.

## Notes on judgment calls

- If the user's brain-dump reveals they actually know very little about the topic, that's a fine outcome — write fewer atomic notes and a longer Learning Queue section. Don't pad confirmed-knowledge notes with things the user didn't actually demonstrate they know.
- If the user explicitly corrects something mid-conversation ("wait, no, that's wrong, actually..."), update your tally accordingly — the *final* stated understanding is what gets written, not the first draft of it.
- Multiple topics in one session (e.g. user starts with "stocks" but wanders into "bonds") are fine — just create/update a separate MOC per topic rather than merging them into one.
