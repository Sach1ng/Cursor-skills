# Cursor setup for PMs

This repo holds Cursor IDE configuration so your AI assistant follows your team’s way of working. Everything lives under **`.cursor/`** and is split into three kinds of things: **Rules**, **Skills**, and **Subagents**.

---

## The three pieces (simple view)

| | What it is | Think of it as |
|---|------------|------------------|
| **Rules** | Persistent instructions that shape how the agent behaves | **Team- or role-specific standards.** How *we* write PRDs, how *we* do reviews, conventions for *this* team or function. Can apply always, or only when certain files are open. |
| **Skills** | On-demand “how-to” the agent uses when the task fits | **Generic PM skills.** Reusable capabilities: writing PRDs, prioritizing action items, drawing diagrams, reviewing strategy. The agent (or you via slash) invokes them when relevant. |
| **Subagents** | Separate mini-agents the main agent calls for a focused job | **Things we actually do.** Concrete activities or workflows, e.g. **VOC reads**, **day-of** execution, research, synthesis. Each runs with its own context so the main chat stays focused. |

**In one line:** Rules = *how we work* (team/role). Skills = *what a PM can do* (generic). Subagents = *specific things we do* (VOC reads, day-of, etc.).

---

## Where things live

| Type | Folder | Example |
|------|--------|--------|
| **Rules** | `.cursor/rules/*.mdc` | Team PRD standards, review checklist |
| **Skills** | `.cursor/skills/<name>/SKILL.md` | prd-writer, action-item-prioritizer |
| **Subagents** | `.cursor/agents/<name>.md` | voc-read, day-of |

Cursor only reads from **`.cursor/`**, so this repo is the single source of truth.

---

## Skills in this repo (generic PM skills)

- **prd-writer** – Intuit-style PRDs (DACE(R), D4D, templates).
- **prd** – Lightweight PRD generator (clarifying questions → `tasks/prd-*.md`).
- **action-item-prioritizer** – Prioritize tasks from summaries, standups, notes.
- **drawbridge** – Excalidraw diagrams (flowcharts, dependency maps).
- **product-strategy-reviewer** – Review product strategy with frameworks.
- **tax-strategist** – Tax planning workflows (entity, deduction, TLH, etc.).

*(Add rules in `.cursor/rules/` for team-specific behavior; add subagents in `.cursor/agents/` for things like VOC reads, day-of, etc.)*

---

## More detail

- **[CURSOR-SETUP.md](CURSOR-SETUP.md)** – Exact difference between rules, skills, and subagents; technical layout and format.

---

## Related

- [PM-skills](https://github.intuit.com/htiwari1/PM-skills-/tree/master) – PM skills in a similar style; this repo uses `.cursor/` so Cursor picks everything up automatically.
- [PM-Operating-System](https://github.intuit.com/htiwari1/PM-Operating-System/tree/master) – PM operating system and workflows (VOC, day-of, etc.); subagents in this repo can mirror those kinds of activities.
