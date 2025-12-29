# F1-Score Interactive Explainer

An interactive explainer for building deep intuition about the F1 score, in the style of Bret Victor's [Ladder of Abstraction](http://worrydream.com/LadderOfAbstraction/).

## Project Status

Early exploration phase. Migrating from Claude iOS chat sessions to this repo for better persistence and organization.

## Skills

### `ladder-evaluation`

A Claude Code skill for evaluating prototypes against Ladder of Abstraction principles. Claude will automatically apply this when reviewing explainer components.

Located in `.claude/skills/ladder-evaluation/`:
- `SKILL.md` - Overview and quick evaluation
- `principles.md` - The three moves, system components, anti-patterns
- `checklists.md` - Detailed evaluation criteria with quality gradients
- `f1-mapping.md` - F1-specific ladder application

## Documentation

- `docs/initial-impressions-ladder-of-abstraction.md` - Initial vision capture

## TODO

### Immediate
- [ ] Export transcripts from previous Claude chat sessions (need browser plugin)
- [ ] Analyze transcripts to extract: design decisions, open questions, prototypes
- [ ] Recreate color system prototype in this repo

### Organization Challenge
- [ ] Design a system to track dependencies between components
- [ ] When concept X changes, know what downstream artifacts need updating
- [ ] Think of project as function: inputs (concepts, constraints) → outputs (explanations, visualizations)

### Content (to be refined after transcript import)
- [ ] Core conceptual explanations
- [ ] Design specs (color system, interaction patterns)
- [ ] Working prototypes

---

*This README will evolve as we import context from previous sessions.*
