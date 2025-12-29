---
name: skill-authoring
description: Guide for creating Claude Code skills. Use when building new skills, structuring skill files, writing skill descriptions, or organizing progressive context loading. Covers SKILL.md format, file organization, and best practices.
---

# Skill Authoring Guide

Create effective Claude Code skills that auto-activate and progressively load context.

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
- [Best Practices](./best-practices.md) - Tips and anti-patterns
