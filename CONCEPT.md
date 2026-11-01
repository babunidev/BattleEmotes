# Battle Emotes — creative concept

**By:** Babuni  
**Project-specific focus:** a dedicated ROARR repository snapshot with an expanded in-game setup tutorial.

## Idea and player experience

The idea behind my **Battle Emotes** experiment was to give an ordinary action press a little character expression. It is closely related to my earlier **Battle Emotes Legacy** project, but this separate repository has its own Git history and a more detailed tutorial. The installed addon remains **ROARR**.

ROARR gives the player a small, characterful flourish while they continue playing World of Warcraft. The player selects one action-bar button. Whenever it is pressed, the addon may call a built-in emote such as ROAR, CHARGE, CHEER, BORED or FLEX. Chance and cooldown controls keep the reactions intermittent, while an enable switch lets the user suspend them without losing configuration.

The source is intentionally narrow. The addon does not fight on the player's behalf, alter ability selection, add damage, construct custom animations or require a GUI. It makes familiar game gestures feel as though the character has a spontaneous personality.

## Why this repository deserves its own record

The separate [`roar` repository](https://github.com/babunidev/BattleEmotesLegacy) already had a ROARR package on November 23, 2025. This `roarr` repository was created later the same day and began with the same basic system. Its unique visible source change is an expansion of `/roarr tutorial` from a one-line summary to **seven numbered setup instructions**.

That addition matters for the experience. Discovering an action slot and adjusting a random-emote tool involves unfamiliar numbers and commands. A guided introduction makes a small, playful addon more approachable without replacing its text-first interface.

Calling this a usability-oriented evolution is an **interpretation of the committed change**. The available repository record does not state the creator's personal motivation for opening a second repo or expanding the tutorial.

## Relationship to other projects

This repo is not mechanically distinct from the first ROARR implementation except for tutorial presentation. It is also **not** a documented direct precursor to every later ROAR-related addon. Link projects by verified changes or explicit creator decisions; do not merge histories merely because their names resemble one another.

My creative direction remains distinct from AI's later work interpreting and documenting the repository. AI-produced documentation and any future technical proposals should be recorded as contributions, not as origin stories.

## Related development history

Battle Emotes, originally the separate `roarr` repository, preserves the same five **hardcoded** native emotes and action-slot/chance/cooldown mechanics as Battle Emotes Legacy. The meaningful source difference is its expanded seven-step `/roarr tutorial`. Neither addon exposes an in-game command for adding emote tokens; that extensible registry appears in the later Roar Guild Addon. The [cross-project development account](docs/EMOTE_FAMILY_HISTORY.md) records the other branches and client targets.
