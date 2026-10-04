# AGENTS.md

Working instructions for coding agents in this repository.

## What this project is

**WastedLands/Skills**: the WastedLands plugin marketplace. Lists WastedLands agent skills for Claude Code (`.claude-plugin/marketplace.json`) and Codex (`.agents/plugins/marketplace.json`). Skills themselves live in their own repos (e.g. `WastedLands/Skill-InitProject`).

**Status (2026-10-04):** draft 0.1.0, private. One plugin listed (`wastedlands`).

## Conventions

- Keep each marketplace entry's `name` identical to the plugin's manifest `name`.
- Entries may reference other repos — Claude: `{"source":"github","repo":"<owner>/<repo>"}`; Codex: `{"source":"url","url":"https://github.com/<owner>/<repo>"}` (verified via install test 2026-10-04). No vendoring.
- The plugin table in `README.md` is generated from the marketplace manifests — don't hand-edit between the `<!-- PLUGINS:START -->` / `<!-- PLUGINS:END -->` markers.
- Validate locally: `claude plugin validate --strict .` and the Codex marketplace-add round-trip in a throwaway home dir.
