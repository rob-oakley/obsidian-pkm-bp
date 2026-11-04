# AGENTS.md

This file provides guidance to AI coding agents when working in this repository.

## Cursor project rules

Cursor loads **`.cursor/rules/*.mdc`** automatically:

| Rule | Scope |
|------|--------|
| `vault-core.mdc` | Always on — structure, safety, defaults |
| `vault-frontmatter.mdc` | All `*.md` — YAML patterns & tags |
| `vault-projects.mdc` | `100_PROJECTS/**` — epics, features, kanban |
| `vault-zettelkasten.mdc` | Atlas, literature notes, scratchpad |
| `vault-agent-definitions.mdc` | `200_AGENTS/**`, `vault_keeper.md` |

This document remains the full reference; rules are concise slices for the agent.

## What This Is

An Obsidian vault (not a code repository) organized with **PARA + ACE + Zettelkasten** methodology. PARA files notes by actionability; ACE provides thinking spaces; Zettelkasten (implemented in Atlas) connects atomic ideas into a web of linked notes. It is a generic personal knowledge management scaffold—populate it with your own projects, domains, and tags.

## Vault Structure

```
pkm-bp/
├── 100_PROJECTS/    — Active projects (deadlines, deliverables)
├── 101_AREAS/       — AoRs (responsibilities) & AoIs (interests)
├── 102_RESOURCES/   — Logs, notes, organizations
├── 200_AGENTS/      — AI agent definitions (markdown system prompts)
├── 201_BASES/       — Obsidian Bases views (.base files)
├── 900_TEMPLATES/   — Note scaffolds
├── 901_ATTACHMENTS/ — Images, screenshots
├── 999_ARCHIVE/     — Completed/retired content
├── ACE/             — Atlas · Calendar · Efforts (thinking layer)
│   ├── Atlas/       — Knowledge maps, MOCs, concepts (Zettelkasten)
│   │   ├── Concepts/ — Permanent atomic notes
│   │   └── MOCs/     — Maps of Content hubs
│   ├── Calendar/    — Temporal notes, Contacts/
│   └── Efforts/     — Active focus tracking
└── INDEX.md         — Main entry point / dashboard
```

**Numbering system is sacred** — never create new top-level numbered prefixes. The ranges are: 100s = PARA content, 200s = AI/agent, 900s = meta/templates, 999 = archive.

## Project Folder Convention

Every project follows this layout:
```
ProjectName/
├── ProjectName.md       — Main overview (Map of Content)
├── Project Kanban.md    — Task board (kanban-plugin format)
├── RE-ENTRY.md          — Context re-entry guide
├── Features/            — Feature specifications
└── Notes & Logs/        — Session logs & working notes
```

## Frontmatter Patterns

All notes use YAML frontmatter. Key patterns:

- **Index pages**: `tags: [index, <category>]` + `aliases:`
- **Projects**: `tags: [projects, active]`, `status:`, `start_date:`, `vertical:`, `tech_stack:[]`, `project: true`
- **Features**: `tags: [feature, <domain>]`, `status: draft|Planning|In Progress|Complete`, `priority:`
- **Contacts** (in ACE/Calendar/Contacts/): `tags: [contact, <org>]`, `role:`, `organization:`, `projects:[]`
- **Agents**: `name:`, `description:`, `version:`, `ai_agent: true`, `status: Active|Draft`
- **Meeting notes**: `tags: [note/meeting, <topic>]`, `meeting_attendees:[]`, `point_of_contact:`
- **Session logs**: Date-prefixed filenames `YYYYMMDD-<Title>.md`
- **Literature notes** (in `102_RESOURCES/Notes/`): `tags: [note/literature, <topic>]`, `type: literature`, `source:`, `created:`
- **Permanent notes** (in `ACE/Atlas/Concepts/`): `tags: [concept, ace/atlas, <topic>]`, `type: permanent`, `status: seed|developing|evergreen`, `created:`
- **MOCs** (in `ACE/Atlas/MOCs/` or `101_AREAS/AoIs/`): `tags: [moc, ace/atlas, <topic>]`, `type: moc`
- **Fleeting notes** (in `SCRATCHPAD` or daily notes): `tags: [inbox, fleeting]`, `type: fleeting`

Boolean flags (`project: true`, `AoR: true`, `AoI: true`, `ai_agent: true`, `idea: true`) and the `type:` field are used by Obsidian Bases for filtered views.

## Linking Conventions

- Use `[[wikilinks]]` for all internal links (Obsidian-native)
- Feature specs link UP to their epic: `[[Project Name]]` below frontmatter
- Epics link DOWN to features in a table
- Index pages have breadcrumb navigation: `[[Parent|← Parent]] | [[INDEX|← Home]]`
- Contact notes link to projects and organizations they're associated with

## Tags

Hierarchical with slashes: `areas/responsibility`, `areas/interest`, `note/meeting`, `note/literature`, `log/incident`, `domain/topic/subtopic` (use your own domain hierarchy). Common top-level: `projects`, `active`, `contact`, `agent`, `index`, `template`, `concept`, `moc`, `zettelkasten`.

## Zettelkasten

Atlas implements Zettelkasten-style linking. See `ACE/Atlas/Zettelkasten.md` for the full methodology.

- **Fleeting** → `SCRATCHPAD` or `ACE/Calendar/` — raw capture
- **Literature** → `102_RESOURCES/Notes/` — source-grounded summaries
- **Permanent** → `ACE/Atlas/Concepts/` — one atomic idea per note
- **MOC** → `ACE/Atlas/MOCs/` or `101_AREAS/AoIs/` — topic hubs

Projects, meeting notes, incident logs, contacts, and feature specs stay in PARA — do not force them into the atomic model.

## Agents

Agent definitions in `200_AGENTS/` are markdown files loaded as system prompts. Structure: Role → Instructions → Constraints → Output Format. The `vault_keeper.md` (root-level) defines vault maintenance workflows and constraints — follow its rules when reorganizing.

## Key Rules

1. **Never delete files** without explicit user confirmation
2. **Never create new top-level numbered folders** — respect the existing numbering
3. **Always add frontmatter** to new notes (tags at minimum)
4. **Report changes before making them** for organizational moves
5. **Maintain Obsidian markdown flavor** — callouts use `>[!type]` syntax
6. **Keep index pages updated** when adding new notes to a category
7. **Feature specs must link bidirectionally** to their parent project

## Obsidian Plugins in Use

`dataview`, `obsidian-git`, `obsidian-kanban`, `templater-obsidian`, `bases` (core). Kanban boards use the `kanban-plugin: board` frontmatter marker with specific settings blocks at the bottom.

## Your domain context

This boilerplate does not assume a job, employer, or tech stack. When you add notes, set `vertical:`, `tech_stack:[]`, and hierarchical tags to match **your** work and interests. Keep employer- or client-specific material in a **private** repo if needed.
