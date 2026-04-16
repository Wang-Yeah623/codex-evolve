# Path Risk Matrix

Use this matrix to decide which rules to load before editing.

| Path | Risk | Why it matters | Load when |
| --- | --- | --- | --- |
| `/` | Medium | Root changes affect the shared scaffold and future sessions. | Starting work from workspace root |
| `/docs` | Low-Medium | Doc drift creates operator confusion and bad handoffs. | Editing documentation |
| `/rules` | High | A bad rule spreads mistakes into future tasks. | Editing reusable policies |
| `/agents` | Medium | Blurry role boundaries make planning, review, and capture collapse together. | Editing role prompts |
| `/memory` | High | Trust in memory depends on append-only, factual records. | Writing or promoting memory |

Notes:

- The nearest `AGENTS.md` overrides generic preferences for its path.
- Add project-specific rows here when a subdirectory develops a stable risk profile.
- If a path is new and high risk, add its rule before relying on repeated memory alone.
