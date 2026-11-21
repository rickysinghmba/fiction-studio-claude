# Fiction Studio for Claude

Fiction-writing plugins for Claude from the [Convert Sprint Writing Studio](https://convertsprintstudio.com/features): a writing partner that drafts in your voice, plans your book, runs nine editors on your chapters (from a development editor to a cold reader panel) and acts on what they find, and follows the craft practices you choose.

## Install (Claude Code)

```
/plugin marketplace add rickysinghmba/fiction-studio-claude
/plugin install fiction-studio@convertsprint
```

Then add the craft plugins you want. Each is optional and installs on its own:

| Plugin | What it does |
| --- | --- |
| `craft-premise-lab` | **Premise lab.** Turns a rough idea into a premise that can carry a whole book. |
| `craft-character-forge` | **Character forge.** Gives each lead a want, a need, a wound, a false belief, an arc and a voice. |
| `craft-outline-stress-test` | **Outline stress test.** Finds the plot holes in your plan before you write them. |
| `craft-fresh-prose` | **Fresh prose.** Catches the stock phrases and habits that make prose sound machine-written. |
| `craft-line-craft` | **Line craft.** Sentence-level discipline: dialogue tags, verbs, rhythm and punctuation. |
| `craft-scene-engine` | **Scene engine.** Every scene wants something, meets resistance, and changes someone. |
| `craft-pacing` | **Pacing & structure.** Tension across the book: no long flat stretches, no endless peaks, a middle that pulls. |
| `craft-setups-payoffs` | **Setups & payoffs.** Tracks the promises your book makes to readers, and whether it keeps them. |
| `craft-continuity` | **Continuity detective.** Contradictions in character, timeline, world rules and facts, with evidence. |
| `craft-dialogue-coach` | **Dialogue coach.** Each character sounds like themselves and only knows what they should. |
| `craft-market-reader` | **Market reader.** A commercial reader's view beside the critic's craft view. |
| `craft-mystery-fair-play` | **Mystery fair play.** Every clue on the page before the reveal, and red herrings that play fair. |
| `craft-romance-beats` | **Romance beats.** The relationship arc readers came for, with both leads changing along the way. |
| `craft-thriller-tension` | **Thriller tension.** A clock that keeps ticking and stakes that rise every chapter. |
| `craft-worldbuilding` | **Worldbuilding.** Magic and technology with costs and limits, shown through the story, never dumped. |
| `craft-serial-hooks` | **Serial hooks.** Every chapter opens fast and ends with a reason to read the next one. |
| `craft-blurb-pitch` | **Blurb & pitch.** Back-cover copy, a one-line hook and a pitch, in the genre's own style. |
| `craft-reader-emails` | **Reader emails.** New-chapter, launch and update emails in your own voice, honest about what's free. |
| `craft-author-bio` | **Author bio & page.** An author bio and author-page copy that sound like the pen name. |
| `craft-store-listing` | **Store listing.** Description, keywords and categories for online bookstores, aimed at the right readers. |

```
/plugin install craft-premise-lab@convertsprint
```

## What's in fiction-studio

- The Writing Studio connector (`https://convertsprintstudio.com/mcp`): Claude reads your books, story bible, plan and timeline, and saves drafts and reviews into your book as suggestions you accept or discard. You sign in the first time.
- Skills: `write-chapter`, `plan-book`, `story-blueprint`, `redraft-round`, `continuity-tidy`, `edit-chapter`, `fix-all`, `decisions`, `preflight`, `book-memory`, `launch-copy`, `craft-plugins`.
- Editor agents: `development-editor`, `story-critic`, `reader-panel`, `accuracy-editor`, `copy-editor`, `proofreader`, `voice-check`, `store-preview`, `guess-the-ending`.

In Claude Code: `/edit-chapter 17` runs Pre-flight and every editor on chapter 17; `/fix-all` acts on what they found.

Everything also works without a studio account, on text you paste or files in your project.

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

## In the Claude app

Download any craft plugin as a skill from Writing Studio → Tools → Craft plugins and add it under Settings → Capabilities → Skills. Add the studio as a connector with `https://convertsprintstudio.com/mcp`.

## About this repository

These files are generated from the Writing Studio's own rules, so the studio and the plugins never disagree. Please open an issue rather than a pull request for changes.

The craft plugins draw ideas from MIT-licensed open-source projects; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). Released under the MIT licence; see [LICENSE](LICENSE).
