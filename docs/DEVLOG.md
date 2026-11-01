# Battle Emotes — development journal for the second repository

**By:** Babuni  
**Reconstructed on:** 2026-10-26 from the source, README, manifest, and Git history of `babunidev/BattleEmotes`. Not a recovered transcript or an account of in-client tests.

## The small idea: let the character answer an action

ROARR turns a routine World of Warcraft action-bar press into a chance for theatrics. A roar, a charge, a flex—or the unexpectedly comic boredom of a fighter in the middle of action—can punctuate an ability without taking control away from the player. The content is intentionally game-native. The addon chooses between built-in `DoEmote` tokens, not a complex bank of voice recordings or custom animations.

The setting is a small act of player-directed expression. Chance, cooldown and an on/off switch determine how often the character interrupts ordinary play. The maker retains creative authority over that experience. This opening is an **interpretation of committed functionality and documentation**, not an invented quote from Babuni's original design conversation.

## Earlier context: the other `roar` repository

The separate [`roar` repository](https://github.com/babunidev/BattleEmotesLegacy) began a day earlier, on 2025-11-22. Its first ROAR implementation noted that it had been rewritten from BuxbrewCharge. By November 23, that repository had passed through several naming changes and had committed ROARR files with a six-second default cooldown and the five emote tokens ROAR, CHARGE, CHEER, BORED and FLEX.

This other repository's history provides **context**, but it is not the development history of `babunidev/BattleEmotes`. It would be misleading to copy every earlier filename experiment into this repository's changelog or imply this repo contained those deleted/renamed files.

## 23 November 2025: the standalone `roarr` repository appears

GitHub records this repository as created on **2025-11-23**. The first substantial commit, `6facf78` at around 14:17 UTC, added the ROARR Lua implementation, TOC, README and MIT license. Its implementation was already recognizable: a global `UseAction` wrapper, a watched slot, editable chance and cooldown, a saved `ROARRDB` preference table and a short `/roarr tutorial` command.

The distribution name, command and manifest were already **ROARR** when committed here. Therefore this repository should not be described as though it independently evolved through the earlier `roar.lua` to `roarr.lua` renames. Those happened in the separate older repository.

The original README emphasized ease of configuration and pure flavor—no combat decisions. The code, meanwhile, makes one subtle mechanical distinction: the cooldown timestamp is set before rolling the probability. A failed roll therefore still requires a cooldown wait. Source comparison today shows the same mechanics in both repositories.

## 23 November 2025: making setup easier

Only minutes after the initial upload, commit `4fc6a68` changed the tutorial block. Previously, typing `/roarr tutorial` produced one condensed line listing commands. It now prints the heading “ROARR setup guide:” followed by **seven numbered instructions**: turn on watch mode and find an action slot, assign a slot, choose chance and cooldown, toggle the addon, read its status, and save.

This is the clearest identifiable **feature improvement unique to this repository**. It does not add a new combat effect. It reduces the information a new user has to infer from a terse command list. The interpretation that this was meant to aid onboarding is plausible from the text, but the Git message and repository do not disclose a first-person reason or discussion. It remains an inferred rationale, not a verified approval record.

## September and October 2026: compatibility wording and documentation

On **2026-09-18**, `6caec00` generalized provider-specific client references to **World of Warcraft 1.12 / Vanilla** terminology. It changed description text, not the emote logic.

On **2026-10-26**, earlier work credited Babuni.dev in the manifest and at the top of README, then placed a minimal concept and technical scaffold in the repo. The footer still contained an older alias; this deeper review standardizes the **display credit** while leaving the MIT license's older copyright notice intact. No historical identity relationship is inferred from those names.

The current documentation pass examined both GitHub repositories and compared their latest Lua sources. After excluding the `tutorial` branch, the two files were **textually identical** at review time. This made it possible to document the difference precisely rather than inventing separate mechanics for the sake of a portfolio story.

## Current state, tests, and next decisions

The snapshot retains one Lua file and one manifest, no automated test suite, no GUI, and no network exchange. The user-configurable battle-emote system is implemented in code but was **not executed in WoW** by this review. A potential saved-variable initialization issue remains: logging in and out without invoking commands or action hooks may overwrite prior settings, because the DB is lazily loaded while logout always saves in-memory state.

Babuni.dev has not yet selected, in evidence available here, which of the two similarly named repositories should be the authoritative public distribution, whether to keep both as historical snapshots, or whether to consolidate them. The documentation leaves those questions open rather than guessing.

**Human direction:** the creator authored/owns the expressive addon concept and decisions. **AI contribution in this pass:** researched the code and history, compared the two sources, authored substantial Markdown documentation and updated the repo; it did not implement new game behavior, perform runtime tests, or decide to merge projects.

## November 2026 — Battle Emotes

After naming the earlier `roar` repository **Battle Emotes Legacy**, I renamed this separate `roarr` repository to **BattleEmotes**. The two snapshots are closely related, but I want their separate histories preserved. The small change that distinguishes this copy in the inspected Git record is its longer seven-step setup tutorial. At my request, an AI assistant aligned this documentation with the new names and first-person viewpoint. The installed addon remains **ROARR**, and no gameplay code was changed or tested during this review.

## 1 November 2026 — distinguishing two very similar repositories

During the comparison of my ROAR experiments, I asked AI to look for a remembered ability to add emotes. Both this repository and Battle Emotes Legacy have the same fixed five-emote pool: the longer tutorial is the distinctive change in this snapshot. The ability to register more native tokens belongs to Roar Guild Addon and its Wrath port, after Multi Action Emotes introduced multiple watched slots. The [family history](EMOTE_FAMILY_HISTORY.md) records the broader chronology without claiming the repositories were formally merged. Documentation only; no game-client testing.
