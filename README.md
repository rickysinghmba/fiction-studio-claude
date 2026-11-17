# Fiction Studio for Claude

Fiction-writing plugins for Claude from the [Convert Sprint Writing Studio](https://convertsprintstudio.com/features): a writing partner that drafts in your voice, plans your book, edits like a copy editor, a development editor or a harsh critic, and follows the craft practices you choose.

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
- Skills: `write-chapter`, `plan-book`, `book-memory`, `launch-copy`, `craft-plugins`.
- Editor agents: `copy-editor`, `development-editor`, `story-critic`.

Everything also works without a studio account, on text you paste or files in your project.

## In the Claude app

Download any craft plugin as a skill from Writing Studio → Tools → Craft plugins and add it under Settings → Capabilities → Skills. Add the studio as a connector with `https://convertsprintstudio.com/mcp`.

## About this repository

These files are generated from the Writing Studio's own rules, so the studio and the plugins never disagree. Please open an issue rather than a pull request for changes.

The craft plugins draw ideas from MIT-licensed open-source projects; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). Released under the MIT licence; see [LICENSE](LICENSE).
