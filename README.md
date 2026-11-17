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
| `craft-fresh-prose` | **Fresh prose.** Catches the stock phrases and habits that make prose sound machine-written. |
| `craft-line-craft` | **Line craft.** Sentence-level discipline: dialogue tags, verbs, rhythm and punctuation. |
| `craft-scene-engine` | **Scene engine.** Every scene wants something, meets resistance, and changes someone. |
| `craft-pacing` | **Pacing & structure.** Tension across the book: no long flat stretches, no endless peaks, a middle that pulls. |
| `craft-setups-payoffs` | **Setups & payoffs.** Tracks the promises your book makes to readers, and whether it keeps them. |
| `craft-continuity` | **Continuity detective.** Contradictions in character, timeline, world rules and facts, with evidence. |
| `craft-dialogue-coach` | **Dialogue coach.** Each character sounds like themselves and only knows what they should. |
| `craft-market-reader` | **Market reader.** A commercial reader's view beside the critic's craft view. |

```
/plugin install craft-fresh-prose@convertsprint
```

## What's in fiction-studio

- The Writing Studio connector (`https://convertsprintstudio.com/mcp`): Claude reads your books, story bible, plan and timeline, and saves drafts and reviews into your book as suggestions you accept or discard. You sign in the first time.
- Skills: `write-chapter`, `plan-book`, `craft-plugins`.
- Editor agents: `copy-editor`, `development-editor`, `story-critic`.

Everything also works without a studio account, on text you paste or files in your project.

## In the Claude app

Download any craft plugin as a skill from Writing Studio → Tools → Craft plugins and add it under Settings → Capabilities → Skills. Add the studio as a connector with `https://convertsprintstudio.com/mcp`.

## About this repository

These files are generated from the Writing Studio's own rules, so the studio and the plugins never disagree. Please open an issue rather than a pull request for changes.

The craft plugins draw ideas from MIT-licensed open-source projects; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). Released under the MIT licence; see [LICENSE](LICENSE).
