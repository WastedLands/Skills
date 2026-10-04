# WastedLands Skills marketplace

Plugin marketplace for WastedLands agent skills.

<!-- PLUGINS:START -->
<!-- This table is generated from the marketplace manifests — do not hand-edit between the markers. -->
| Plugin | Skills | Description |
|---|---|---|
| `wastedlands` | `init-project` | Interview-driven scaffolding for new software projects |
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

## Adding a skill

Skills live in their own repos (e.g. [`WastedLands/Skill-InitProject`](https://github.com/WastedLands/Skill-InitProject)). To list a new plugin here, add an entry to `.claude-plugin/marketplace.json` (and `.agents/plugins/marketplace.json` for Codex) pointing at the skill repo — no vendoring needed. Keep entry `name` identical to the plugin's manifest `name`.
