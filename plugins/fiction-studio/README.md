# Fiction Studio for Claude

Claude as a fiction-writing partner that works in your own book. It connects Claude to the Convert Sprint Writing Studio, so Claude drafts in your voice from the studio's brief and saves drafts and editor reviews straight into your manuscript as suggestions you accept or discard.

## What you get

- **Writing Studio connector**: Claude can read your books, story bible, plan and timeline, and save drafts, plans and reviews. You sign in to the studio the first time Claude uses it.
- **Skills**: `write-chapter` (draft, continue or redraft), `plan-book` (premise, chapter plans, clues, timeline), `story-blueprint` (check the plan's architecture before drafting or a big redraft), `redraft-round` (several chapters redrafted side by side without breaking the book), `continuity-tidy` (cross-chapter continuity, story bible and timeline after every round), `edit-chapter` (Pre-flight and every editor on a chapter, in one go), `fix-all` (act on what the editors found, asking only about real choices), `decisions` (the story choices no edit may undo), `preflight` (free machine checks), `launch-copy` (blurb, tagline, pitch, reader emails, bio, store listing), `book-memory` (promise ledger and story so far) and `craft-plugins` (choose which practice packs to switch on for a book).
- **Editor agents**: `development-editor`, `story-critic`, `reader-panel`, `accuracy-editor`, `copy-editor`, `proofreader`, `voice-check`, `store-preview` and `guess-the-ending`.

In Claude Code, type `/edit-chapter 17` for the full editor pass on chapter 17, then `/fix-all`.

Everything works without the studio too, on text you paste or files in your project; you just can't save into a book.

## Install (Claude Code)

```
/plugin marketplace add rickysinghmba/fiction-studio-claude
/plugin install fiction-studio@convertsprint
```

Then add any craft plugins you want, one per pack:

- `craft-premise-lab`: Turns a rough idea into a premise that can carry a whole book.
- `craft-character-forge`: Gives each lead a want, a need, a wound, a false belief, an arc and a voice.
- `craft-outline-stress-test`: Finds the plot holes in your plan before you write them.
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

## Let long passes run without stopping

Claude Code asks before each studio tool call until you allow it, so a full editor pass or a redraft round can stop dozens of times for a yes. To let them run through, add an allow rule for the studio's tools to your project's `.claude/settings.json`:

```json
{
  "permissions": {
    "allow": ["mcp__plugin_fiction-studio_convertsprint-writing-studio__*"]
  }
}
```

If you connected the studio another way (for example as a connector on your Claude account), its tools carry that connector's name instead: `/mcp` shows it, and the rule is `mcp__<that name>__*`. Drafts and reviews still arrive as suggestions you accept or discard, and the skills still show you a preview and wait for your yes before anything goes into your book.

## In the Claude app

Add the Writing Studio as a connector (`https://convertsprintstudio.com/mcp`), and upload any craft plugin as a skill: download its zip from Writing Studio → Tools → Craft plugins, then add it in the Claude app under Settings → Capabilities → Skills.

## Lessons learned

From a long revision of a real mystery novel, now built into the skills and editors:

1. **Fix the architecture before the prose.** Four rounds of chapter redrafts barely moved a harsh critic, because the problems were in the plan. `story-blueprint` checks the plan before drafting and before any big redraft round.
2. **Every tell needs a twin.** The culprit was guessed because only she triggered one behaviour. The tell inventory makes each clue point at a second suspect too, or marks it as the one fair tell.
3. **Keep a world-rule ledger.** State the rule once, early; plant every exception before it's used; anything new after the midpoint is rule creep. Costs are one number per scene, never a recap.
4. **Decisions have costs.** When editors' advice runs into a saved decision, Claude says roughly what it costs and asks once whether to reopen it.
5. **Plan, redraft side by side, then tidy. Always.** `redraft-round` writes each chapter's sets-up and pays-off contract first, gives every agent its own scratch folder and a fresh read of its chapter, and ends with `continuity-tidy` across the chapters, the story bible and the timeline.
6. **Test fairly.** Guess-the-ending prompts never hint at the culprit, run in their own folder, record guesses at each checkpoint before reading on, and run once per question. Critic scores move about half a star between runs: compare two runs before calling a change a win.
7. **Invented details stay invented.** Phone numbers in the 555-01xx range, and no real companies or products.
8. **Every book grows its own tics.** The voice check and copy editor keep a per-book tic list with limits and check it on every pass.
9. **Tidy the small things.** Every chapter opens the same way, and every word has one spelling (grey or gray, not both).
10. **Fewer interruptions.** Pre-allow the studio's tools so long passes don't stop for permission (see above).

## Credits

The craft plugins draw ideas from MIT-licensed open-source projects; see THIRD_PARTY_NOTICES.md in the marketplace repository.
