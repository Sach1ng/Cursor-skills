# Cursor Setup: Skills, Rules, and Subagents

This doc explains the **exact difference** between the three Cursor concepts and how this repo is organized.

---

## Simple mental model (for PMs)

- **Rules** = **Team- or role-specific.** How *we* work: our PRD format, review standards, conventions. Can be scoped to a function or team.
- **Skills** = **Generic PM skills.** Reusable capabilities: PRDs, prioritization, diagrams, strategy review. The agent (or you) invokes them when the task fits.
- **Subagents** = **Concrete things we do.** Specific activities or workflows the main agent delegates: e.g. **VOC reads**, **day-of** execution, research, synthesis. Each runs in its own context.

See also: [PM-Operating-System](https://github.intuit.com/htiwari1/PM-Operating-System/tree/master) for workflows that map well to subagents (VOC, day-of, etc.).

---

## Quick comparison (technical)

| | **Skills** | **Rules** | **Subagents** |
|---|------------|-----------|----------------|
| **What** | On-demand capabilities (how-to, workflows, domain knowledge) | Persistent instructions (standards, conventions) | Specialized agents that run in parallel with their own context |
| **When used** | Loaded when relevant; can be invoked via slash or by the agent | Always (or by file/glob); part of initial context | Delegated by main agent for discrete subtasks |
| **Location (project)** | `.cursor/skills/<name>/SKILL.md` | `.cursor/rules/*.mdc` | `.cursor/agents/<name>.md` |
| **Location (user)** | `~/.cursor/skills/` | (rules are project-level) | `~/.cursor/agents/` |
| **Format** | Dir with `SKILL.md` + optional refs/scripts | Single `.mdc` file with frontmatter | Single `.md` file with frontmatter + system prompt body |
| **Best for** | Generic PM skills: PRDs, diagrams, prioritization, strategy review | Team/role-specific: our standards, our format | Concrete activities: VOC reads, day-of, research, synthesis |

---

## Skills

- **Role:** Teach the agent *how* to do specific tasks when they’re relevant.
- **Behavior:** Not always in context. The agent discovers and applies them when the description matches the task; you can also invoke via slash (e.g. `/prd-writer`).
- **Content:** Procedures, templates, examples, optional scripts. Keep `SKILL.md` under ~500 lines; use `reference.md` / `examples.md` for more.
- **YAML:** `name`, `description` (description drives when the skill is used).

**Use for:** PRDs, diagrams (Drawbridge), action-item prioritization, tax strategy, product strategy—any “when you do X, follow this process.”

---

## Rules

- **Role:** Steer behavior in the background (coding standards, conventions, “never do X”).
- **Behavior:** Included in context based on mode: **Always apply**, **Apply intelligently**, **Apply to specific files** (globs), or **Apply manually** (@mention).
- **Content:** Short, actionable (e.g. “use this pattern,” “avoid this”). One concern per rule; aim for &lt; 50 lines.
- **Format:** `.mdc` in `.cursor/rules/` with frontmatter: `description`, `globs` (optional), `alwaysApply` (optional).

**Use for:** Team- or role-specific standards (e.g. our PRD format, review checklist). Can apply to the whole project or only when certain files are open.

---

## Subagents

- **Role:** Separate agents that handle a *part* of the main agent’s job, in parallel, with their own context and tools.
- **Behavior:** Main agent delegates subtasks (e.g. “explore codebase,” “run tests,” “review code”). Each subagent has its own context window and system prompt.
- **Content:** System prompt in the `.md` body; frontmatter has `name` and `description` (when to delegate).
- **Location:** Project: `.cursor/agents/<name>.md`. User: `~/.cursor/agents/<name>.md`. Project overrides user for same name.

**Use for:** Concrete activities you delegate: e.g. **VOC reads**, **day-of** execution, research, synthesis. Each runs in its own context so the main chat stays focused.

---

## How this repo is organized

- **Skills:** `.cursor/skills/`  
  One folder per skill, e.g. `prd-writer/`, `drawbridge/`, `action-item-prioritizer/`, etc.
- **Rules:** `.cursor/rules/`  
  Optional; add `.mdc` files here when you want project-wide or file-specific rules.
- **Subagents:** `.cursor/agents/`  
  Optional; add `<name>.md` here when you want custom subagents (e.g. code-reviewer, debugger).

Cursor only reads **`.cursor/`** for skills, rules, and agents. The `.agents/` folder is not used by Cursor; any content there has been aligned with `.cursor/` (e.g. skills live under `.cursor/skills/`).

---

## Reference: PM-skills-style layout

If you’re aligning with a repo that uses an `.agents/`-style layout (e.g. [PM-skills](https://github.intuit.com/htiwari1/PM-skills-/tree/master)):

- **For Cursor:** Use `.cursor/skills/` so the editor and CLI discover skills.
- **For consistency with PM-skills:** You can keep a copy or symlink under `.agents/skills/` for documentation or tooling that expects that path, but Cursor will only use `.cursor/skills/`.

This repo standardizes on **`.cursor/`** as the single source of truth for Cursor.
