# Fiction Studio for Claude

Claude as a fiction-writing partner that works in your own book. It connects Claude to the Convert Sprint Writing Studio, so Claude drafts in your voice from the studio's brief and saves drafts and editor reviews straight into your manuscript as suggestions you accept or discard.

## What you get

- **Writing Studio connector**: Claude can read your books, story bible, plan and timeline, and save drafts, plans and reviews. You sign in to the studio the first time Claude uses it.
- **Skills**: `write-chapter` (draft, continue or redraft), `plan-book` (premise, chapter plans, clues, timeline), `launch-copy` (blurb, tagline, pitch, reader emails, bio, store listing) and `craft-plugins` (choose which practice packs to switch on for a book).
- **Editor agents**: `copy-editor`, `development-editor` and `story-critic`.

Everything works without the studio too, on text you paste or files in your project; you just can't save into a book.

## Install (Claude Code)

```
/plugin marketplace add rickysinghmba/fiction-studio-claude
/plugin install fiction-studio@convertsprint
```

Then add any craft plugins you want, one per pack:

- `craft-fresh-prose`: Catches the stock phrases and habits that make prose sound machine-written.
- `craft-line-craft`: Sentence-level discipline: dialogue tags, verbs, rhythm and punctuation.
- `craft-scene-engine`: Every scene wants something, meets resistance, and changes someone.
- `craft-pacing`: Tension across the book: no long flat stretches, no endless peaks, a middle that pulls.
- `craft-setups-payoffs`: Tracks the promises your book makes to readers, and whether it keeps them.
- `craft-continuity`: Contradictions in character, timeline, world rules and facts, with evidence.
- `craft-dialogue-coach`: Each character sounds like themselves and only knows what they should.
- `craft-market-reader`: A commercial reader's view beside the critic's craft view.
- `craft-mystery-fair-play`: Every clue on the page before the reveal, and red herrings that play fair.
- `craft-romance-beats`: The relationship arc readers came for, with both leads changing along the way.
- `craft-thriller-tension`: A clock that keeps ticking and stakes that rise every chapter.
- `craft-worldbuilding`: Magic and technology with costs and limits, shown through the story, never dumped.
- `craft-serial-hooks`: Every chapter opens fast and ends with a reason to read the next one.
- `craft-blurb-pitch`: Back-cover copy, a one-line hook and a pitch, in the genre's own style.
- `craft-reader-emails`: New-chapter, launch and update emails in your own voice, honest about what's free.
- `craft-author-bio`: An author bio and author-page copy that sound like the pen name.
- `craft-store-listing`: Description, keywords and categories for online bookstores, aimed at the right readers.

## In the Claude app

Add the Writing Studio as a connector (`https://convertsprintstudio.com/mcp`), and upload any craft plugin as a skill: download its zip from Writing Studio → Tools → Craft plugins, then add it in the Claude app under Settings → Capabilities → Skills.

## Credits

The craft plugins draw ideas from MIT-licensed open-source projects; see THIRD_PARTY_NOTICES.md in the marketplace repository.
