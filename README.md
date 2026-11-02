# Technically Dark Academia — Virtual Library

A virtual bookshop and library where curiosity becomes an explorable place.

**Current repository status (2026-11-02):** early concept, original narrative content, and environment art direction. This repository does **not** yet contain a playable game or a Steam build.

## The first playable experience

Enter a recognizable, human-scale bookshop at blue hour. Discover books through shelves and covers. Pick up an item and read an available, rights-permitted passage or a clearly fictional demo text. Select a phrase to unfold marginalia and a deeper thread of ideas. Save the thought as Markdown. Switch between Explore, Study, Research and Quiet modes without losing your place.

The first version is **entirely virtual and simulated**, with no live bookshop inventory or real-world space synchronization. A future Sydney bookshop integration is an aspiration, not an implemented feature.

## Materials

- [Art direction and everyday-bookshop product anchor](docs/ART_DIRECTION.md): primary visual and browsing principles.
- [Player-facing content pack](docs/CONTENT_PACK.md): draft copy and sample journals.
- [Claude creative handoff](docs/CLAUDE_CREATIVE_HANDOFF.md): implementation review criteria.
- [Existing concept-art set](assets/concept/): everyday bookshop, grand bookshop and living page.
- [Experience and content design v0.1](content/experience-seed-v0.1.md): narrative premise, rooms, first 90 seconds, modes, interaction contracts and MVP checks.
- [Original fictional volume seed data](content/books.seed.json): five fictional **demo reading fixtures (not real books for sale)** with opening passages, marginalia and research threads.
- [Margin Table — reading alcove concept](art/concepts/tda-margin-table-v01.png): additional environment concept for the deep-reading interaction, **not** a functional UI screenshot.
- [Index Alcove — additional environment concept](art/concepts/tda-index-alcove-v01.png): concept illustration for spatial and material direction; **not** a finished game level or asset pack.

## Design commitments

- A functional reading experience matters more than elaborate ambient decoration.
- Readers control the depth of disclosure and own their notes.
- Simulated books, actual bibliographic records and sourced real-world facts are never conflated.
- Keyboard access, legibility, optional low-motion viewing and graceful 2D inspection are first-class requirements.
- UI strings stay in data/localisation files, not baked into art.
- Any future public-domain book text must be verified per work, edition, country, and rights status.

## For implementers

Begin with the interaction vertical slice and the existing seed JSON. Keep content loading engine-agnostic and schema versioned. Do not treat the concept illustration as measured architecture or a finished 3D model.

## Rights

Original writing and generated concept imagery are provided here as in-progress project materials. No open-source licence or broad reuse permission is implied by their presence in a public repository; the owner will determine publishing and reuse terms.
