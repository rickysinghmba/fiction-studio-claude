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

## Without the studio

If the Writing Studio connector isn't connected (its tools such as `list_projects` aren't available), work on the text the writer gives you or the files open in this project instead, and say once that connecting the studio lets you save drafts and reviews straight into their book. Keep a "Decisions" list at the top of the project notes and read it before every draft or edit.
