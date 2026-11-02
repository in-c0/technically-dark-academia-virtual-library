# Technically Dark Academia — Content & Experience Seed v0.1

> A virtual bookshop and library that makes curiosity feel like entering a place.  
> **Status:** original narrative and interaction direction, not a claim of implemented gameplay.

## Product premise

TDA begins as a self-contained virtual space on desktop/Steam. The everyday, human-scale bookshop in `docs/ART_DIRECTION.md` is the primary first-playable browsing reference. This document contributes a **focused deep-reading and marginalia vertical slice**, not a replacement for that broader product direction. The five accompanying invented volumes are explicitly labeled demo fixtures, never presented as real published or purchasable books. There is **no live synchronization with a physical bookshop** in this first release. Public catalogue data may enrich discoverability later, but fictional shelves, simulated stock, and real-world bibliographic records must be clearly distinguished.

The central interaction is not simply browsing a 3D room. A reader should be able to:

1. **Notice** a book, passage, sound or object in an atmospheric environment.
2. **Approach and open** it, immediately finding useful or intriguing content.
3. **Unfold context** progressively: a phrase, a marginal note, a linked idea, a source, a room, an entire subject.
4. **Carry the discovery away** into a chosen note-taking system, initially through a reliable Markdown copy/export action.
5. **Change the room's behaviour** to fit their intention without losing reading position or context.

The space is an interface to thinking, not merely a decorated catalogue.

## Experience pillars

- **Atmosphere with agency:** lighting, ambience, and detail support presence, but never obstruct reading or navigation.
- **Depth on demand:** each object offers a light first glance; further information only unfolds if invited.
- **One place, different intentions:** study, research, explore, and do-not-disturb are different behaviours of the same persistent environment.
- **User-owned thoughts:** notes and highlights are exportable; no mandatory account or proprietary lock-in for the prototype.
- **Truthful provenance:** original fiction, externally sourced facts, and simulated world-state have explicit provenance.
- **Accessibility by design:** keyboard navigation, high contrast/readable text, reduced motion, independent ambience controls, and a flat 2D inspection mode.

## Opening sequence: 90-second vertical slice

**00:00–00:20 — Arrival.** The player enters a blue-hour bookshop. A single quiet lamp illuminates a handwritten index and a small cluster of interesting books. The camera stays still until the player acts. A discreet instruction: “Follow what catches your eye.”

**00:20–00:40 — Discovery.** Hover/focus a volume: its title and one-line invitation appear. Select **The Book of Living Worlds**. The book moves into a readable inspection view, with no required long animation.

**00:40–01:00 — Unfolding.** Open its first spread. A short original passage appears. Select the phrase *a city that kept its weather indoors* to reveal a marginal note. Expand that note into a thematic research card. Back navigation retains the exact page and selection.

**01:00–01:15 — Take something with you.** Select one sentence and choose **Keep this thought**. A clean Markdown note preview contains title, excerpt, location, provenance, and a space for the player's own thoughts. A working **Copy Markdown** control is enough for v0.1; third-party note integrations are deferred.

**01:15–01:30 — Change intention.** Select **Study**. Ambience fades, motion reduces, reading becomes the visual priority, and an optional session timer appears. The open book and context are preserved.

## Modes

| Mode | Reader intent | Behaviour | Must preserve |
| --- | --- | --- | --- |
| **Explore** | Wander and be surprised | Richer environmental cues, gentle recommendations, spatial navigation | Discoveries and navigation history |
| **Study** | Concentrate on one text | Stable camera, reduced animation, clear reading surface, optional timer | Page, highlights, notes |
| **Research** | Follow connections | Expandable source/provenance panel, idea links, working notes and comparison slots | All source citations and navigation trail |
| **Quiet / Do Not Disturb** | Minimize interruptions | Muted notifications, reduced decorative motion, low-intensity audio, subdued UI | Every active task; no forced modal |

Modes are independent of room location. Avoid creating four different “worlds” that fragment user state.

## First rooms

### The Blue-Hour Atrium
Optional atmospheric / later-zone interpretation; the initial browsable shop should follow the everyday-bookshop anchor. Entry and playful discovery. Tall shelving, a broad window, warm pools of practical reading light, and an armillary sculpture. No floating feature-menu billboards. A small cluster of hand-authored books guides the first interaction.

### The Margin Table
A close, comfortable, usable desk that makes deep reading and note-taking feel tangible. Book, selected passage, marginalia, research expansion and export are the main visual hierarchy. This is the **first interaction to fully implement**.

### The Index Alcove
A quieter collection of relationships: subjects, questions, books, fragments, places. It should be navigable as semantic links or accessible lists, not depend on decorative physical filing cabinets.

## Microcopy (English canonical strings)

| Key | Copy |
| --- | --- |
| `arrival.invitation` | Follow what catches your eye. |
| `book.inspect` | Open this book |
| `passage.expand` | Unfold this thought |
| `context.back` | Return to the page |
| `notes.keep` | Keep this thought |
| `notes.copy` | Copy Markdown |
| `notes.copied` | Copied. Take it wherever you think best. |
| `mode.explore` | Explore |
| `mode.study` | Study |
| `mode.research` | Research |
| `mode.quiet` | Quiet |
| `source.original` | Original fiction created for TDA |
| `world.simulated` | Fictional collection · simulated world |
| `empty.no_results` | Nothing here yet. The shelves are still growing. |

Localisation note: all text should be keyed and independently translated. Never bake UI labels into scene textures.

## Interaction/content contract

The companion `books.seed.json` is content, not the authoritative schema of the eventual engine. Every seeded volume has:

- A stable `id`, title, subtitle, author display, shelf, subject tags.
- An original teaser and opening passage.
- Three disclosure layers: surface impression, margin annotation, research thread.
- A reusable `note_prompt` to invite original thought.
- A `provenance` marker: distinguish fiction from sourced factual records.

### Sample note export

```md
# The Book of Living Worlds — thought

> [Selected passage]

Source: TDA original fiction  
Volume: The Book of Living Worlds  
Location: opening spread

My thoughts:
```

When real-world books are integrated later, store accurate author, edition, licence, link, and text-source information; never silently invent availability or full-text rights.

## Visual direction for concept art

- **Palette:** ink-black woods, weathered bronze, desaturated deep green, soft parchment, blue-hour ambient light and warm localized reading light.
- **Mood:** exploratory and lived-in, intellectually abundant without ornamental clutter.
- **Camera:** human eye-level, meaningful sightlines, readable book/desk scale.
- **Spatial priority:** large surfaces and interactive reading objects are visually legible.
- **Avoid:** generic fantasy magic glows, excessive particles, unearned gothic horror, illegible text, decorative UI as world geometry.
- **Distinguish:** concept paintings ≠ production-ready game assets, layout plans, or validated scene implementations.

## Proposed MVP acceptance checks

1. Player can inspect and read a seeded volume with mouse **and** keyboard.
2. One selection opens a margin note and a deeper research layer; closing each returns to previous context.
3. A selected excerpt produces accurate Markdown that can actually be copied.
4. Switching four modes preserves page, selections and notes; Quiet minimizes interruptions.
5. Text remains usable at 1080p and supports a larger font/reduced motion option.
6. No fictional book or simulated shelf is presented as real-world availability.
7. A new `books.seed.json` volume can be added without hardcoding its contents into the scene.

## Boundaries

This initial narrative packet does **not** implement a Steam release, a 3D scene, licensed book text, external note-platform APIs, user accounts, real inventory, recommendations, or runtime content generation. Those each need separate decisions, tests and rights checks.

**Rights:** the seed writing is an original draft for the TDA project; publication and licensing terms are reserved for the owner to decide. No third-party book excerpts are included.
