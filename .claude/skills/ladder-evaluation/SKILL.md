---
name: ladder-evaluation
description: Evaluate interactive explainers against Bret Victor's Ladder of Abstraction principles. Use when reviewing prototypes, checking if visualizations support fluid movement between concrete and abstract levels, or assessing whether an explainer enables genuine understanding vs just showing information.
---

# Ladder of Abstraction Evaluation

Evaluate interactive explainers using Bret Victor's framework for understanding complex systems.

## When to Use This Skill

- Reviewing a prototype or visualization
- Checking if an explainer supports the three moves (Control, Abstract, Step Down)
- Assessing transition quality between abstraction levels
- Identifying gaps in the "ladder" coverage

## Quick Evaluation (Start Here)

Ask these three questions:

1. **Can the user control parameters and see immediate feedback?** (Control)
2. **Can the user see all possibilities at once?** (Abstract)
3. **Can the user click abstract → see concrete instance?** (Step Down)

If any answer is "no" or "partially," dig deeper with the full checklists.

## The Central Insight

> "The deepest insights are born not at any one level of abstraction, but in the **transitions between them**."

The goal is **intuitive understanding**, not just information display.

## Progressive Evaluation

Load these as needed:

- [Core Principles](./principles.md) - The three moves, system components, anti-patterns
- [Evaluation Checklists](./checklists.md) - Detailed criteria with quality gradients
- [F1 Score Mapping](./f1-mapping.md) - Specific application to our F1 explainer

## Evaluation Output Format

When evaluating, report:

```
## Evaluation: [Component Name]

### Level: [Concrete / Mid / Abstract]

### Checklist Results
- Control: [❌/🟡/✅] [notes]
- Abstract: [❌/🟡/✅] [notes]
- Step Down: [❌/🟡/✅] [notes]
- Transitions: [❌/🟡/✅] [notes]

### Key Gaps
- [What's missing or broken in the ladder]

### Recommendations
- [Specific fixes to improve ladder coverage]
```
