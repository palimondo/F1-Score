---
name: skill-authoring
description: Create and evolve Claude Code skills. Use when building new skills, structuring skill files, writing descriptions, capturing session learnings as skill refinements, or updating skills from latest documentation. Covers SKILL.md format, progressive loading, versioning, and learning patterns.
---

# Skill Authoring

Create and evolve Claude Code skills that auto-activate and progressively load context.

## When to Use This Skill

- Building a new skill from scratch
- Structuring skill files for progressive loading
- Writing effective skill descriptions
- Capturing session learnings as skill refinements
- Updating skills based on new documentation
- Versioning and evolving existing skills

## What is a Skill?

A markdown module that teaches Claude specialized knowledge. Unlike slash commands:
- **Auto-activates** when request matches the description
- **Progressively loads** supporting files on demand
- **No explicit invocation** required

## Quick Start

1. Create directory: `.claude/skills/your-skill-name/`
2. Add `SKILL.md` with required frontmatter
3. Add supporting files for progressive loading
4. Commit and push

## SKILL.md Template

```yaml
---
name: lowercase-with-hyphens
description: Clear explanation of what and when. Use action verbs
  and specific trigger terms. Max 1024 chars.
---

# Skill Title

Brief overview (1-2 sentences).

## When to Use

- Trigger condition 1
- Trigger condition 2

## Quick Reference

[Essential info that fits in ~100 lines]

## Progressive Loading

- [Detailed reference](./reference.md)
- [Examples](./examples.md)
```

## Key Rules

| Rule | Details |
|------|---------|
| Name format | Lowercase, hyphens, max 64 chars |
| Description | Action verbs, specific triggers, max 1024 chars |
| SKILL.md size | Keep under 500 lines |
| Supporting files | Load on demand via relative links |

## More Details

- [File Structure](./structure.md) - Organization patterns
- [Best Practices](./best-practices.md) - Tips, anti-patterns, official docs
- [Skill Evolution](./evolution.md) - Versioning, updating from docs, learning from experience
