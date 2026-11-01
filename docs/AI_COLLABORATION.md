# Battle Emotes — collaboration and attribution methodology

**By:** Babuni.

## What the existing evidence can tell us

The public README, `roarr.lua`, `roarr.toc`, license and Git history establish what this repository contains and when specific files changed. They do **not** provide an original conversation explaining why a second ROARR repo was started or who suggested each line of Lua.

Keep my creative direction distinct from implementation details. Avoid assigning the idea of built-in action-triggered emotes to AI just because AI assists with later documentation or coding.

## This documentation pass

On **2026-10-26**, an AI assistant:
- Read the committed ROARR Lua, TOC, README, LICENSE and previous short documentation files.
- Inspected the initial upload and the November 23 tutorial-update diff.
- Compared the current Lua source with that in the separate `babunidev/roar` repository; all text except the `tutorial` branch was identical.
- Identified the timing of the cooldown and source-observable edge cases.
- Expanded public project documentation and standardized README display author credit.

That is an attributable **analysis/editing contribution**. It is not evidence that AI conceived the original project, authored all historical code, or ran it successfully.

## Attribution and permission boundaries

My public identity for this project is **Babuni**; **babuni.dev** is the wider development portfolio. The preserved MIT license includes a historical `Copyright (c) 2025 Elexior` notice. Do not change it without the proper rights context. Avoid republishing old private chats, player messages, sensitive data or third-party material as part of the public development record.

## Future journal entries must include

1. What Babuni.dev requested and why.
2. What AI proposed, including options/limitations.
3. What the creator accepted, rejected or deferred.
4. Which files/commits changed and how they differ from the previous state.
5. Exact tests run, environment and observed results.
6. What remains unverified.

In the absence of any of these, explicitly label retrospective inference or proposed work rather than completing the narrative with fiction.

## November 2026 — documenting my naming choice

I renamed this repository from `roarr` to **BattleEmotes**, keeping it distinct from **BattleEmotesLegacy**. My AI assistant reviewed the existing record and updated its titles, links and attribution at my request. The original `ROARR` addon files and historic MIT copyright statement remain unchanged. No runtime verification was performed.

## Related development history

Battle Emotes, originally the separate `roarr` repository, preserves the same five **hardcoded** native emotes and action-slot/chance/cooldown mechanics as Battle Emotes Legacy. The meaningful source difference is its expanded seven-step `/roarr tutorial`. Neither addon exposes an in-game command for adding emote tokens; that extensible registry appears in the later Roar Guild Addon. The [cross-project development account](EMOTE_FAMILY_HISTORY.md) records the other branches and client targets.
