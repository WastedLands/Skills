# WastedLands Skills marketplace

Plugin marketplace for WastedLands agent skills.

<!-- PLUGINS:START -->
<!-- This table is generated from the marketplace manifests — do not hand-edit between the markers. -->
| Plugin | Skills | Description |
|---|---|---|
| `wastedlands` | `init-project` | Interview-driven project scaffolding: idea → structured repo (AGENTS.md, docs, OpenSpec, CI) |
<!-- PLUGINS:END -->

## Use

**Claude Code:**

```bash
claude plugin marketplace add WastedLands/Skills
claude plugin install wastedlands@wastedlands
```

**Codex:**

```bash
codex plugin marketplace add WastedLands/Skills
codex plugin add wastedlands@wastedlands
```

Invoke plugin skills with the plugin namespace, e.g. `$wastedlands:init-project` (tested on Codex CLI). A standalone skill copied into `~/.agents/skills/` is invoked without it, e.g. `$init-project`.

> Both CLIs add the marketplace over git. If a marketplace add fails with an auth error, authenticate first: `gh auth login`, or an SSH key with access to the org (`ssh -T git@github.com` should greet you).

## Adding a skill

Skills live in their own repos (e.g. [`WastedLands/Skill-InitProject`](https://github.com/WastedLands/Skill-InitProject)). To list a new plugin here, add an entry to `.claude-plugin/marketplace.json` (and `.agents/plugins/marketplace.json` for Codex) pointing at the skill repo — no vendoring needed. Keep entry `name` identical to the plugin's manifest `name`.
