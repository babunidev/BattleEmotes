# Battle Emotes — development rules

**By:** Babuni.

## Read before changing anything

Review `README.md`, `CONCEPT.md`, `docs/DEVLOG.md`, `docs/DECISIONS.md`, `roarr.lua`, `roarr.toc` and the separate `roar` repository only when making a comparison. This repository is **`babunidev/BattleEmotes`**, not `babunidev/BattleEmotesLegacy`; do not edit the other repo accidentally.

## Preserve provenance

1. Attribute the project's purpose, character direction and any approved creative choices to Babuni.
2. Credit AI for identifiable analysis, suggestions, authored code or documentation separately. Do not infer who conceived a feature merely from a source file.
3. Treat the November 2025 seven-step tutorial revision as a documented implementation difference, not proof of an unseen approval discussion.
4. Keep the two GitHub histories separate. Never merge, rename, archive or delete one without explicit direction.
5. Keep historical MIT license attribution intact. Existing copyright line `2025 Elexior` is a rights statement, not disposable display branding.
6. Every substantial implementation requires a changelog, narrative devlog, decision/update record and accurate test results. Retrospective inference must be labeled.

## Engineering constraints

- Target WoW 1.12/Lua 5.0-compatible APIs unless Babuni directs otherwise.
- Preserve original action execution when intercepting `UseAction`.
- Understand that a missed chance roll consumes cooldown under current code.
- `ROARRDB` is account-wide, but lazily loaded; test no-interaction logout carefully.
- Ensure emote tokens exist on the target client before claiming support.
- Do not manufacture gameplay test results from source inspection.
- Keep all secrets and private player chats out of public documentation.

The 2026-10-26 work was documentation-only and did not approve runtime changes.

## First-person project narrative and naming

The GitHub repository is **BattleEmotes** (display title **Battle Emotes**), formerly `roarr`. The older `roar` repository is now **BattleEmotesLegacy**. Both installed packages historically use **ROARR**, so keep their Git histories distinct. Do not rename `roarr.lua`, `roarr.toc`, `/roarr` or `ROARRDB` without explicit approval.

Use **Babuni** for the human identity, **babuni.dev** for the development portfolio, and **creative** rather than “creator” as a role label. In public narratives write from Babuni's first-person viewpoint, never beginning a narrative sentence with `I` or `My`. Present AI as an assistant who contributed documented work, not the narrator or original author. Preserve uncertain history and the historical MIT copyright line.

## Cross-project evidence

Use [the family-history comparison](docs/EMOTE_FAMILY_HISTORY.md) before describing this project's relationship to Battle Emotes Legacy, Multi Action Emotes, or Roar Guild Addon. Do not imply the static five-token source array is an unlimited player-editable emote list.

## Repository-local documentation standard

Before writing or changing project documentation, read [docs/DOCUMENTATION.md](docs/DOCUMENTATION.md). These rules travel with this repository and do not depend on the babuni.dev ChatGPT Project. Preserve all project-specific technical, creative, canon, safety, licensing, and historical rules in this file; follow the linked standard for public first-person narrative, human–AI attribution, concise development journals, decision records, and evidence-based verification. **Babuni** is the human creative; **babuni.dev** is the website/portfolio, not the person. Preserve third-party credits and historical legal notices. References above to a dated “documentation-only audit” describe that past task, not a permanent ban on later authorized implementation.
