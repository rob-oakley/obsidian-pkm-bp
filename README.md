# obsidian-pkm-bp

Obsidian vault scaffold for personal knowledge management: **PARA + ACE + Zettelkasten**. Use it as a starting point for projects, areas, literature notes, and atomic concepts.

Inside Obsidian, open **`INDEX.md`** for the vault dashboard.

## Prerequisites

- [Obsidian](https://obsidian.md/) (desktop recommended for first setup)
- [Git](https://git-scm.com/)
- SSH access to GitHub (or use HTTPS clone URL if you prefer)

Optional:

- [GitHub CLI](https://cli.github.com/) (`gh`) for repo management
- **Obsidian Git** community plugin if you want commit/pull/push from inside Obsidian

## Local setup

Do **not** use Obsidian’s “Create new vault” wizard to generate a fresh vault with sample plugins and settings. Those files can conflict with this repo. Instead, start from an **empty folder** and clone this repository into it.

### 1. Create an empty vault folder

Pick where the vault should live (example paths; use your own):

```bash
mkdir -p ~/Obsidian\ Vaults/pkm-bp
cd ~/Obsidian\ Vaults/pkm-bp
```

The directory must be **empty** before clone (no existing `.obsidian` or notes).

### 2. Clone into that folder

Clone with `.` so the vault root is the git repository root:

```bash
git clone git@github.com:rob-oakley/obsidian-pkm-bp.git .
```

HTTPS:

```bash
git clone https://github.com/rob-oakley/obsidian-pkm-bp.git .
```

### 3. Open the folder in Obsidian

1. Obsidian → **Open folder as vault**
2. Select the folder you cloned into (e.g. `pkm-bp`)
3. Trust the vault if prompted

If Obsidian already had a different vault at this path, remove or rename the old folder first, then clone again.

### 4. Install community plugins

This repo tracks **which** plugins you use, not the plugin bundles (see `.gitignore`).

1. **Settings → Community plugins → Turn on community plugins**
2. **Browse** and install plugins listed in `.obsidian/community-plugins.json`:
   - **Excalidraw** (`obsidian-excalidraw-plugin`)
3. Enable each installed plugin

Other plugins referenced in vault docs (e.g. Kanban, Templater, Dataview) are optional; add them when you need them.

### 5. Sync changes

From the vault root:

```bash
git pull    # get latest
git add -A
git commit -m "Describe your change"
git push
```

Or install **Obsidian Git**, point it at this folder, and sync from the Obsidian command palette.

## What gets synced

| Tracked | Ignored (local only) |
| ------- | -------------------- |
| Notes, templates, `ACE/`, PARA folders | `.obsidian/workspace.json` (window layout) |
| Minimal `.obsidian/` config | `.obsidian/plugins/` (reinstall via step 4) |
| `.cursor/rules/` for Cursor agents | `.DS_Store`, secrets (`.env`, keys) |

## Vault layout (short)

```
100_PROJECTS/   Active projects
101_AREAS/      Areas of responsibility & interest
102_RESOURCES/  Literature, logs, reference
200_AGENTS/     AI agent definitions
900_TEMPLATES/  Note templates
ACE/            Atlas · Calendar · Efforts
INDEX.md        Start here in Obsidian
```

Full conventions: **AGENTS.md** (for Cursor) and **vault_keeper.md** (organization rules).

## Cursor / AI agents

If you use [Cursor](https://cursor.com/) with this vault, open the cloned folder as the project workspace. Agent guidance lives in **AGENTS.md** and `.cursor/rules/`.

## License / visibility

Check repository visibility on GitHub before storing employer or sensitive data. Prefer a **private** repo for work-related notes.
