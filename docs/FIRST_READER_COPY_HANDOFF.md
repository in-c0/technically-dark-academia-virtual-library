# TDA — First-reader copy & journal prompt handoff (EN/KO)

**Status:** content-only editorial draft, 2026-11-03. **Not integrated into a playable build, visually inspected in-game, or release-approved.**

This package gives the implementation team keyed, bilingual copy for the existing `content/experience-seed-v0.1.md` deep-reading slice. It does not introduce an engine, require a new feature, or change the original fictional book dataset.

## Files

- `content/locales/en.json` — English source strings (61 keys).
- `content/locales/ko.json` — Korean translations for the same keys.
- `content/journal-prompts.seed.json` — the 12 existing original prompts from `docs/CONTENT_PACK.md`, paired with new Korean translations.

All content is an **editorial draft**. Book titles, body text, and research threads in `content/books.seed.json` remain English. This is **not** full Korean localization.

## Minimum player encounter

1. **Enter:** `arrival.invitation` → `arrival.enter`. The optional `arrival.wander` and `arrival.find_subject` actions do not require an account.
2. **Browse:** Discover a book in shelf context, not only through search. This repository's five invented books must display `book.demo_label` and provenance; never pose as real, purchasable stock.
3. **Read:** `book.inspect` → original passage → `passage.expand` → `context.go_deeper` → `context.back`. Closing context must return to the exact page/selection.
4. **Keep:** `notes.keep` → editable thought → `notes.preview` → `notes.copy`. Show `notes.copied` only on verified clipboard success, `notes.copy_failed` when it fails. The note should include accurate book/fixture attribution and text location.
5. **Change intention:** `mode.explore`, `mode.study`, `mode.research`, `mode.quiet` should change behaviors without losing the passage, selection, or note. Show `status.saved_position` only after state preservation is working.

The five book fixtures already have `surface`, `margin`, and `research` layers and stable cross-links. Do not require new content fields or hardcode any particular book ID into UI.

## Content truth conditions

| String or action | Only show when |
| --- | --- |
| `book.demo_label`, `status.demo_collection` | The user is viewing this **fictional, simulated** collection. |
| `book.preview` | A real-world preview is available under verified use rights; do not imply TDA hosts the whole book. |
| `book.no_text`, `book.provider_link` | Text cannot be displayed locally; an actual provider URL must exist before offering the link. |
| `book.no_verified_edition` | Edition metadata cannot be verified. Do not fill gaps with invented facts. |
| `context.no_sources` | A fiction passage has no linked external sources. Do not turn thematic links into purported research citations. |
| `notes.private_local` | The note is local/ephemeral and export or copy is possible; do not imply cloud storage, permanent save, or encryption. |
| `status.saved_position` | Mode switching genuinely retains reading context in the live implementation. |
| `mode.quiet.hint` | Quiet mode reduces actual distractions. Do not claim social messaging is paused before messaging exists. |

In particular, the presence of UI strings does **not** authorize marketing claims about working functions, public-domain full text, live inventories, AI generation, social presence, VR, or Steam readiness.

## Integration conventions

- Lookup uses one stable string key with a selected locale; use English fallback only for missing translations, and log/test missing keys.
- Let the reader choose language independently of operating system locale. Do not change language in the middle of a note without preserving user text.
- Keep `en.json` and `ko.json` key sets identical. Never bake labels into textures/concept art.
- Keep functional labels legible at 1080p. Check Korean text expansion, line wraps, control focus, and contrast in an actual render.
- Respect keyboard and 2D reading view paths; `accessibility.keyboard_hint` is help text, not evidence that keyboard support works.
- A copy failure must retain selectable text; loss of clipboard permission must not lose the note.
- The 12 journal prompts are optional invitations. Never convert them into required quests, streaks, or productivity pressure.
- Prompt source text and translations are fiction/creative invitations, not facts, quotations from real books, or evidence of actual player activity.

## Verification required after game integration

- [ ] On first launch, a reader can browse without login or forced tutorial.
- [ ] Five fixture books are clearly labelled original fiction, not for sale.
- [ ] Mouse and keyboard reach the same text, marginalia, research, and back navigation.
- [ ] Expanding and closing context restores the original selection and scroll position.
- [ ] Copy Markdown produces the actual chosen passage and correct provenance; denial/failure is recoverable.
- [ ] Changing each of four modes retains selected book, page, marginalia state, and unsaved note text.
- [ ] A 2D reading path works without navigating the 3D environment.
- [ ] English and Korean strings display without clipping at 1080p and with larger text.
- [ ] Reduced motion and ambient audio controls actually affect behavior.
- [ ] No unsupported feature copy is surfaced as shipped functionality.

**Known naming decision:** `docs/CONTENT_PACK.md` sometimes calls the browsing mode “Browse”; `content/experience-seed-v0.1.md` calls it **Explore**. The keyed UI follows **Explore** for this draft. Align product vocabulary before release; this package does not change earlier source documents.

**Creative boundary:** This work is text and data only. It does not replace production-quality environment art, UI implementation, functional testing, or the original browsing-first product direction.
