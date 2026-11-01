# Battle Emotes — in-game words, built-in emotes and tutorial

This content inventory belongs to my **Battle Emotes** repository, formerly `roarr`. Its five built-in emote tokens are part of the historical **ROARR** addon rather than new assets created in this documentation revision.

**By:** Babuni.  
**Source:** `roarr.lua`.

## Five built-in emote tokens

| Token | Player-facing flavor |
| --- | --- |
| `ROAR` | A fierce, loud interruption |
| `CHARGE` | Momentum and battle spirit |
| `CHEER` | Encouragement/celebration |
| `BORED` | Wry comic contrast |
| `FLEX` | Strength and bravado |

The game client supplies the exact animation or rendered emote wording for these built-in tokens. ROARR does not embed five original audio recordings, custom animations or five custom text scripts.

Fallback when `DoEmote` is unavailable: `SendChatMessage("makes a battle cry!", "EMOTE")`. The fallback is written in the addon; whether it is needed/allowed on a particular server is unverified.

## Tutorial text

This snapshot's unique added content is an expanded `/roarr tutorial` sequence. Rather than one compact hint, it prints a **title** and **seven numbered steps** about watch, slot, chance, cooldown, on/off, info and save. It is authored directly in `roarr.lua`, not loaded from an external content or localization file.

## Configuration/status messages

The chat UI prints `ROARR:` plus descriptions for enabled, disabled, watched slot, saved settings, errors and `info`. This source supports English-only author-supplied guidance. Localization of Blizzard's built-in emote output is controlled by the game, not by this addon.

For future content revisions, preserve authorship and distinguish the creator's source text from the game-owned built-in emote tokens. Record specific accepted changes and tested behavior rather than silently replacing content.

## Related development history

Battle Emotes, originally the separate `roarr` repository, preserves the same five **hardcoded** native emotes and action-slot/chance/cooldown mechanics as Battle Emotes Legacy. The meaningful source difference is its expanded seven-step `/roarr tutorial`. Neither addon exposes an in-game command for adding emote tokens; that extensible registry appears in the later Roar Guild Addon. The [cross-project development account](EMOTE_FAMILY_HISTORY.md) records the other branches and client targets.
