# WastedLands Skills marketplace

Plugin marketplace for WastedLands agent skills. Currently hosts one plugin:

| Plugin | Skills | Description |
|---|---|---|
| `wastedlands` | `init-project` | Interview-driven scaffolding for new software projects |

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

(The Codex marketplace JSON schema is still draft — verify during local testing.)

## Adding a skill

Skills live in their own repos (e.g. [`WastedLands/Skill-InitProject`](https://github.com/WastedLands/Skill-InitProject)). To list a new plugin here, add an entry to `.claude-plugin/marketplace.json` (and `.agents/plugins/marketplace.json` for Codex) pointing at the skill repo — no vendoring needed. Keep entry `name` identical to the plugin's manifest `name`.
