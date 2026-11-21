---
name: decisions
description: "Keep the list of story choices the author made on purpose (\"Danny loses one memory a night\", \"the late-night call stays unexplained\") so no draft or editor undoes them. Use when the writer settles a question, says 'keep it' or 'that's deliberate', or asks what's been decided."
---

# The author's decisions

A decision is a story choice the author made on purpose. Every writing and editor brief carries the list and tells Claude never to undo one, so editors raise a problem as a note instead of quietly reversing it.

## With the Writing Studio connected

- **See them:** `get_decisions` for the book.
- **Add one:** when the writer settles something (answers an editor's question, says "keep it", "that's on purpose", "yes, she's lying"), offer to record it in one plain sentence, with the chapter it starts from. Call `save_decision` only once they agree. Write what was decided, not why an editor objected.
- **Remove one:** when the writer changes their mind, `save_decision` with `remove_id`.
- Keep the list short and current (up to 40 per book): one decision per choice, no duplicates, nothing an editor could mistake for a rule of grammar.

## What a decision costs

A decision protects a choice; it doesn't make the choice free. In one real revision, protected decisions were the main reason the critic's score stopped rising, and nobody said so. So when an editor's advice runs into a decision:

- Don't skip it silently, and don't keep suggesting it round after round.
- Say once, plainly, what it costs: "Keeping the late-night call unexplained costs roughly half a star on Plausibility: the critic and two of the panel's readers stopped believing there." Use the editors' own scores and notes for the estimate, and say it's rough.
- Ask once whether the writer wants to reopen it (AskUserQuestion when you can: keep it, or reopen it). If they keep it, don't raise it again until something changes; if they reopen it, remove the decision and plan the change.

## The book's tic list

Every book grows its own tics: words and phrases the author (or Claude) reaches for again and again ("peat", "fingertips", "cellar-cold", "two and a half years"). Keep them as one decision, so every brief carries it: `House tics (at most per chapter): peat 1, fingertips 1, cellar-cold 0, "two and a half years" 1 in the book`. Add a tic when an editor or Pre-flight spots a new one and the writer agrees; the voice check, copy editor and proofreader check it on every pass.

## Without the studio

If the Writing Studio connector isn't connected (its tools such as `list_projects` aren't available), work on the text the writer gives you or the files open in this project instead, and say once that connecting the studio lets you save drafts and reviews straight into their book. Keep a "Decisions" list (with the tic list as one entry) at the top of the project notes and read it before every draft or edit.
