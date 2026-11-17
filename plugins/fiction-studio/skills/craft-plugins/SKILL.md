---
name: craft-plugins
description: "Help the writer choose which craft plugins (fiction-writing practice packs such as Fresh prose, Pacing & structure or Dialogue coach) to switch on for a book, and switch them on. Use when the writer asks about craft plugins, writing rules, or what Claude checks for."
---

# Choose craft plugins

Craft plugins are optional packs of fiction-writing practice. Each adds rules for whoever writes, checks for the editors, and sometimes phrases for the automatic AI-phrasing check. They suggest; the writer decides.

## With the Writing Studio connected

1. `list_craft_plugins` for the book. Each comes with what it does, what it changes, who it's good for and who should skip it, and whether it's installed.
2. Describe the options briefly in the writer's terms and recommend two or three for this book, given its genre and where the draft is. Say why.
3. Only after the writer says which they want, call `set_craft_plugins` with the full list of ids to have on.
4. From then on, `get_writing_brief` and `get_editor_brief` include their rules for that book.

They can also be switched on in the studio: Writing Studio → Tools → Craft plugins.

## In Claude itself

The same packs install as Claude plugins from the `convertsprint` marketplace, one per pack, so they apply to any writing in Claude:

- `craft-premise-lab`: Premise lab. Turns a rough idea into a premise that can carry a whole book.
- `craft-character-forge`: Character forge. Gives each lead a want, a need, a wound, a false belief, an arc and a voice.
- `craft-outline-stress-test`: Outline stress test. Finds the plot holes in your plan before you write them.
- `craft-fresh-prose`: Fresh prose. Catches the stock phrases and habits that make prose sound machine-written.
- `craft-line-craft`: Line craft. Sentence-level discipline: dialogue tags, verbs, rhythm and punctuation.
- `craft-scene-engine`: Scene engine. Every scene wants something, meets resistance, and changes someone.
- `craft-pacing`: Pacing & structure. Tension across the book: no long flat stretches, no endless peaks, a middle that pulls.
- `craft-setups-payoffs`: Setups & payoffs. Tracks the promises your book makes to readers, and whether it keeps them.
- `craft-continuity`: Continuity detective. Contradictions in character, timeline, world rules and facts, with evidence.
- `craft-dialogue-coach`: Dialogue coach. Each character sounds like themselves and only knows what they should.
- `craft-market-reader`: Market reader. A commercial reader's view beside the critic's craft view.
- `craft-mystery-fair-play`: Mystery fair play. Every clue on the page before the reveal, and red herrings that play fair.
- `craft-romance-beats`: Romance beats. The relationship arc readers came for, with both leads changing along the way.
- `craft-thriller-tension`: Thriller tension. A clock that keeps ticking and stakes that rise every chapter.
- `craft-worldbuilding`: Worldbuilding. Magic and technology with costs and limits, shown through the story, never dumped.
- `craft-serial-hooks`: Serial hooks. Every chapter opens fast and ends with a reason to read the next one.
- `craft-blurb-pitch`: Blurb & pitch. Back-cover copy, a one-line hook and a pitch, in the genre's own style.
- `craft-reader-emails`: Reader emails. New-chapter, launch and update emails in your own voice, honest about what's free.
- `craft-author-bio`: Author bio & page. An author bio and author-page copy that sound like the pen name.
- `craft-store-listing`: Store listing. Description, keywords and categories for online bookstores, aimed at the right readers.

Install with `/plugin install <name>@convertsprint`.
