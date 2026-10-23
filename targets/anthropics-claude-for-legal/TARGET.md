# anthropics/claude-for-legal

| | |
|---|---|
| Publisher | Anthropic |
| Licence | Apache-2.0 |
| Version read | 4a6c651889c97cc9140580363c73e0eb17379c2b (committed 2026-07-23 00:46 UTC; upstream head on 2026-10-15) |
| Entries in this release | 2 |

A repository of 12 plugins for legal work (150 `SKILL.md` files, counted at upstream head 4a6c651889 on 2026-10-15) plus one vendor plugin under `external_plugins/cocounsel-legal` and five managed-agent cookbooks. Each plugin ships skill instructions, a plugin-level `CLAUDE.md` guardrail file and a `.mcp.json` connector list; the skills are read by a model at run time and are not scored. The only test artifacts recorded are `scripts/test-cookbooks.sh` and two validators named in CONTRIBUTING.md (`scripts/lint-tool-scope.py`, which checks tool scope, and `scripts/validate.py`, which validates managed-agent output against a schema).

## How corrections are accepted

Pull request. CONTRIBUTING.md requires the contributor licence agreement to be accepted on the first pull request and asks for a plugin version bump on a material change.
