# TDA — Creative Handoff for Claude / Implementation Team

Read **docs/ART_DIRECTION.md** and **docs/CONTENT_PACK.md** before building or publishing game-facing UI. This creative pack is meant to be integrated into the real game, not copied into a generic slideshow or placeholder scene.

## Public artwork
- assets/concept/tda-everyday-bookshop.png — **primary emotional reference** for the actual first playable bookshop. A plausible, airy, quiet, human-scale bookstore with diverse covers.
- assets/concept/tda-grand-bookshop.png — **aspirational TDA flagship** reference for broader world direction, not an already-built location.
- assets/concept/tda-living-page.png — **speculative interaction illustration** for 'Imagine this place', not a production render or proof of 3D scene generation.

All three are AI-generated concept illustrations. They have been visually inspected as still illustrations, **not** evaluated as finished Steam promotional assets, game scenes, or functional features.

## Product truth
The initial game is virtual-first. No real Dymocks partnership, real-world live occupancy, live physical shelf synchronization, in-world commerce, full copyrighted e-book access, or guaranteed VR support exists by virtue of this content pack. Do not imply otherwise in UI, marketing, or demos.

## Creative acceptance criteria
1. On entering, books and human-scale browsing take precedence over a menu/dashboard.
2. The visitor can wander with no goal; no forced quest, streak, or onboarding registration.
3. A book can be discovered from its shelf context, not only search.
4. Switching Browse/Study/Research/Solitude never discards the current reading/notebook context.
5. Actual avatars (if implemented) are distinguished from simulated occupants; privacy and messaging are independently controlled.
6. The original player journals are clearly fictional sample content, not actual published titles.
7. External book metadata is attributable and terms-compatible; only licensed/permitted previews may be displayed.
8. The 'Imagine' concept, if unimplemented, is explicitly marked future/speculative and never faked.
9. UI text is editorially restrained, not generic gamey achievements or overstated AI marketing.
10. Validate the actual build and inspect real screenshots before calling any Steam imagery final.

## First requested output back to Ava
Share a real interactive build or recording of the *book browsing loop*, plus screenshots from representative camera positions, technical limitations, and a list of planned vs implemented features. Review it against the art direction before preparing Steam artwork. Do not pass concept illustrations as screenshots.

## Content implementation
The game-copy file contains a draft Steam short/long description, entry flow, 10 environment zones, in-world microcopy, 12 journaling prompts, 3 original journal entries, and initial Korean localization. Use it as source material. Publish Steam copy only after checking every stated feature against a verified build.


## Supplemental deep-reading slice (2026-11-02)

A separate, testable reading-and-notes content package is now available:
- `content/experience-seed-v0.1.md` — staged 90-second reading loop, progressive disclosure, four modes and acceptance checks.
- `content/books.seed.json` — **five original fictional demo fixtures**, with marginalia and research links. They are **not real published books, current stock, licensed excerpts, or sale listings**.
- `art/concepts/tda-margin-table-v01.png` and `art/concepts/tda-index-alcove-v01.png` — additional AI-generated environment concept paintings. Not game geometry, UI, or verified scene renders.

Treat `docs/ART_DIRECTION.md`'s human-scale **everyday bookshop** as the primary first-playable setting. The supplemental reading slice belongs inside that broader experience and must not replace real-book browsing with a fictional catalogue. For offline proof-of-interaction, label demo fixtures in-world and include a provenance indicator.

Minimum demonstrable implementation: open a fixture; inspect a passage; select an annotated phrase; expand a second context layer; return to the exact reading position; copy a truthful Markdown excerpt/note; switch Browse/Study/Research/Quiet without discarding state. Verify actual keyboard use and a readable 1080p view. Report what is implemented separately from planned.
