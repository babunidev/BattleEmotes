# Battle Emotes — source-backed decisions and open questions

**Creative director:** Babuni.dev.

## What is actually established

| Topic | Evidence | Status |
| --- | --- | --- |
| Existing action button drives emotes | `UseAction` wrapper in `roarr.lua` | Implemented |
| Five game-native gestures rather than custom media | `DoEmote` token pool | Implemented |
| Configurable probability, cooldown, disable switch | `/roarr` commands | Implemented |
| Account-wide saved state | TOC `SavedVariables: ROARRDB` | Implemented, not cross-character tested |
| Longer tutorial in this repository | 2025-11-23 `4fc6a68` diff | Implemented and historically dated |
| Second repository with near-identical code | content comparison with `babunidev/roar` | Verified at source level, reason unknown |
| Current chance roll consumes interval even on failure | `LAST_BATTLE_EMOTE_TIME = now` before `math.random` | Source-observed; may be reconsidered |

## Historical boundaries

The repository `babunidev/BattleEmotes` was created and populated on November 23, 2025. The `babunidev/roar` repository existed earlier and shows multiple ROAR/ROARR renames. This repo did **not** experience those historical renames itself in its visible Git record.

The presence of a duplicate-like repo does not establish an intent to abandon the other one. The tutorial change is verified as a source change; an original user/AI design debate is not available.

## Attribution and license

The current README and TOC credit **Babuni.dev** as author. The MIT `LICENSE` contains a historical `Elexior` copyright line. Both facts are retained; no conclusion is made about identity or rights transfers. This documentation-only pass does not edit license text.

## Open creator decisions (not approved)

- Which ROARR repository should be considered canonical for distribution?
- Would the creator prefer to keep this repo as a historical experiment or archive it?
- Should the tutorial evolve further into a low-noise or accessible onboarding flow?
- Should chance failures consume cooldown?
- Should per-character configuration replace account-wide slot selection?
- Should the historic license attribution be clarified?

The AI assistant must record explicit author answers before changing code or repo governance.

## November 2026 — repository identity

I renamed the repository to **BattleEmotes**, with the public title **Battle Emotes**, and kept the earlier **BattleEmotesLegacy** repository separate. This does not rename the installed **ROARR** addon or merge the two Git histories. At my request, AI updated the documentation only.

## Related development history

Battle Emotes, originally the separate `roarr` repository, preserves the same five **hardcoded** native emotes and action-slot/chance/cooldown mechanics as Battle Emotes Legacy. The meaningful source difference is its expanded seven-step `/roarr tutorial`. Neither addon exposes an in-game command for adding emote tokens; that extensible registry appears in the later Roar Guild Addon. The [cross-project development account](EMOTE_FAMILY_HISTORY.md) records the other branches and client targets.
