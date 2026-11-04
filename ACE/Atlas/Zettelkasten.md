---
tags:
  - index
  - ace/atlas
  - zettelkasten
aliases:
  - Zettelkasten
---

# Zettelkasten

> A personal knowledge management system that uses interconnected atomic notes to build a web of thoughts.

[[Atlas|← Atlas]] | [[ACE|← ACE]] | [[INDEX|← Home]]

---

## How Zettelkasten Fits PARA + ACE

| System | Question it answers |
|--------|---------------------|
| **PARA** | *Where does this file belong?* (Projects, Areas, Resources, Archive) |
| **ACE** | *How do I think about this?* (Atlas, Calendar, Efforts) |
| **Zettelkasten** | *How do ideas connect?* (Atomic notes linked into a web) |

PARA files notes by actionability. Zettelkasten (implemented in **Atlas**) connects ideas across those folders. They are complementary — not competing systems.

---

## Note Types

| Type | Location | Purpose | Frontmatter |
|------|----------|---------|-------------|
| **Fleeting** | [[SCRATCHPAD]] or `ACE/Calendar/` daily notes | Raw capture, disposable | `type: fleeting` |
| **Literature** | `102_RESOURCES/Notes/` | Source-grounded summaries | `type: literature`, `source:` |
| **Permanent** | `ACE/Atlas/Concepts/` | One atomic idea, evergreen | `type: permanent`, `status: seed\|developing\|evergreen` |
| **MOC** | `ACE/Atlas/MOCs/` + AoIs in `101_AREAS/AoIs/` | Topic hubs that index concepts | `type: moc` |

---

## Lifecycle

```
Capture → Distill → Atomize → Connect
```

1. **Capture** — Jot fleeting notes in [[SCRATCHPAD]] or a daily note. Don't organize yet.
2. **Distill** — Process capture into a literature note with source attribution and key ideas.
3. **Atomize** — Extract one idea per permanent note in [[Concepts]]. Title = a claim; body = explanation + links.
4. **Connect** — Link permanent notes into [[MOCs]] and domain AoIs. Surface relevant concepts in projects.

---

## Permanent Note Rules

- **One idea per note** — If you need "and also…", split into two notes.
- **Title is a claim** — "D.A.R.T diagnoses before analyzing" not "D.A.R.T Framework Notes".
- **Minimum 2 outbound wikilinks** — Every permanent note connects to at least two other notes.
- **Link up to MOCs** — Every concept should be reachable from at least one MOC.

---

## When NOT to Zettelkasten

These note types stay in PARA — do not force them into the atomic model:

- Project overviews, feature specs, and Kanban boards → `100_PROJECTS/`
- Meeting notes and session logs → `ACE/Calendar/` or project `Notes & Logs/`
- Incident logs → `102_RESOURCES/`
- Contacts → `ACE/Calendar/Contacts/`
- Agent definitions → `200_AGENTS/`

---

## Frontmatter Reference

```yaml
# Literature note (102_RESOURCES/Notes/)
tags: [note/literature, <topic>]
type: literature
source: <url or citation>
created: YYYY-MM-DD

# Permanent atomic note (ACE/Atlas/Concepts/)
tags: [concept, ace/atlas, <topic>]
type: permanent
status: seed | developing | evergreen
created: YYYY-MM-DD

# MOC (ACE/Atlas/MOCs/ or 101_AREAS/AoIs/)
tags: [moc, ace/atlas, <topic>]
type: moc
```

---

## Templates

- [[Literature Note Template]] — Source-grounded summaries
- [[Atomic Note Template]] — Permanent concept notes
- [[MOC Template]] — Topic hub notes

---

## Related

- [[Concepts]] — Index of permanent atomic notes
- [[MOCs]] — Index of Maps of Content
- [[Mental Models]] — Example MOC
