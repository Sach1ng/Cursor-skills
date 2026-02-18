# .agents folder

This folder is **not** used by Cursor for skills, rules, or subagents.

- **Cursor reads only from `.cursor/`.** See the repo root [CURSOR-SETUP.md](../CURSOR-SETUP.md) and [README.md](../README.md).
- Skills that were here (e.g. `skills/prd/`) have been mirrored into `.cursor/skills/` so Cursor can discover them.
- You can keep `.agents/` for compatibility with repos like [PM-skills](https://github.intuit.com/htiwari1/PM-skills-/tree/master) or remove it; the single source of truth for this repo is `.cursor/`.
