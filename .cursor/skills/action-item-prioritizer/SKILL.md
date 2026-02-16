---
name: action-item-prioritizer
description: Prioritize action items and tasks based on strategic goals. Use when reviewing Slack summaries, daily updates, meeting notes, or any list of tasks and action items. Helps identify what to focus on first.
---

# Action Item Prioritizer

## Current Strategic Goals

When prioritizing action items, evaluate against these key goals (in order of priority):

### Goal 1: E3B Lite - Meet 45K GNS
- **Metric**: Gross New Starts (GNS)
- **Focus**: Customer acquisition, sales pipeline, conversion optimization
- **High-priority signals**: Leads, demos, trials, onboarding, pricing discussions, customer objections, sales blockers

### Goal 2: E3B Full Service - Hit 500 Paying Customers
- **Metric**: Paying customer count
- **Focus**: Running experiments, testing hypotheses, measuring results
- **High-priority signals**: Experiment results, A/B tests, customer feedback, churn analysis, activation metrics, retention strategies

## Prioritization Framework

When presented with action items, categorize and rank them:

### Priority Tiers

| Tier | Criteria | Action |
|------|----------|--------|
| **P0 - Critical** | Directly blocks goal progress, time-sensitive, customer-facing issue | Do immediately |
| **P1 - High** | Directly advances goals, has clear impact on metrics | Do today |
| **P2 - Medium** | Supports goals indirectly, enables future progress | Schedule this week |
| **P3 - Low** | Nice to have, no clear goal connection | Delegate or defer |

### Scoring Rubric

For each action item, assess:

1. **Goal Alignment** (0-3): How directly does this advance E3B Lite or Full Service goals?
   - 3 = Directly moves key metric
   - 2 = Enables someone else to move metric
   - 1 = Indirectly related
   - 0 = No connection

2. **Urgency** (0-3): What's the time sensitivity?
   - 3 = Blocking others or has deadline today
   - 2 = Needed this week
   - 1 = Needed this month
   - 0 = No deadline

3. **Impact** (0-3): What's the potential effect?
   - 3 = High impact on customers/revenue
   - 2 = Moderate impact
   - 1 = Low impact
   - 0 = Minimal impact

**Priority Score** = Goal Alignment + Urgency + Impact (max 9)
- 7-9: P0 Critical
- 5-6: P1 High  
- 3-4: P2 Medium
- 0-2: P3 Low

## Output Format

When prioritizing action items, produce output in this format:

```markdown
## Prioritized Action Items

### P0 - Critical (Do Now)
- [ ] [Action item] — *Goal: [E3B Lite/Full Service], Impact: [brief reason]*

### P1 - High (Do Today)
- [ ] [Action item] — *Goal: [E3B Lite/Full Service], Impact: [brief reason]*

### P2 - Medium (This Week)
- [ ] [Action item] — *Goal: [E3B Lite/Full Service], Impact: [brief reason]*

### P3 - Low (Delegate/Defer)
- [ ] [Action item] — *Reason for deferral*

### Recommended Focus
Top 3 items to focus on today:
1. [Item] - [30-second why]
2. [Item] - [30-second why]
3. [Item] - [30-second why]
```

## Usage Examples

**Example input**: "Follow up with customer X about pricing, review Q4 experiment results, update team wiki, respond to partner inquiry about integration"

**Example output**:
```
### P0 - Critical
- [ ] Follow up with customer X about pricing — *Goal: E3B Lite 45K GNS, Impact: Active sales opportunity*

### P1 - High
- [ ] Review Q4 experiment results — *Goal: E3B Full Service, Impact: Informs next experiment cycle*
- [ ] Respond to partner inquiry — *Goal: E3B Lite, Impact: Potential channel growth*

### P2 - Medium
- [ ] Update team wiki — *Reason: Enables team efficiency but not directly goal-aligned*
```

## VIP Senders (Auto-Escalate to P1)

Messages from these people are automatically P1 - High priority:
- **Brandon (bmitchell4)** - Strategic leadership, always prioritize

## Quick Deprioritization Signals

Items to push to P3 or delegate:
- Internal process documentation (unless blocking others)
- Meetings without clear agenda tied to goals
- Reports not driving decisions
- "Nice to have" features
- Tasks others can own

## Goal Updates

If goals change, update this section:
- Last updated: January 2026
- E3B Lite target: 45K GNS
- E3B Full Service target: 500 paying customers
