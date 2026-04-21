# AGENTS.md

## Repo purpose
This repository contains a personal knowledge workflow project for Obsidian.

The project has two parts:
1. A local sync/import tool that mirrors Xiaomi-exported markdown notes into `源池/`
2. An Obsidian plugin that lets the user select text in a note and append it to `摘录池/` with one click

## Non-goals
- Do not build a full standalone note-taking app
- Do not add cloud sync
- Do not add mobile support
- Do not add AI auto-classification
- Do not rewrite the user's original notes

## Data safety rules
- Never perform whole-repo overwrite
- The sync tool may only modify `源池/`
- The plugin may only append/update files under `摘录池/`
- Preserve user-created files outside managed directories
- Keep all outputs as plain markdown files

## Product priorities
1. Data safety
2. Fast selection -> classify flow
3. Long markdown note stability
4. Simple architecture
5. Easy future migration to a standalone desktop app

## Implementation preferences
- Prefer the smallest working version first
- Keep dependencies minimal
- Add a clear README for local testing
- If a task is large, plan first before coding
- Explain major file changes before implementation

## Done means
- Core flow works end-to-end on sample notes
- Sync only touches `源池/`
- Classification only writes to `摘录池/`
- Build/test commands are documented
- Output markdown remains readable without the plugin
