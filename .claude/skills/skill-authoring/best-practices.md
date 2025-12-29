# Skill Authoring Best Practices

## Writing Effective Descriptions

The description determines when Claude activates the skill. Make it specific:

### Weak Descriptions
```yaml
description: Helps with documents
description: Useful tool for coding
description: General helper
```

### Strong Descriptions
```yaml
description: Extract text and tables from PDF files, fill forms,
  merge documents. Use when working with PDFs or document extraction.

description: Evaluate interactive explainers against Ladder of
  Abstraction principles. Use when reviewing prototypes or checking
  if visualizations support fluid movement between abstraction levels.
```

### Description Checklist
- [ ] Includes action verbs (extract, evaluate, generate, validate)
- [ ] Lists specific trigger terms users would say
- [ ] States explicit "Use when..." conditions
- [ ] Under 1024 characters

---

## Progressive Disclosure

### Do: Keep SKILL.md Focused
```markdown
# Overview
Brief intro.

## Quick Reference
Essential info only.

## Details
- [Full reference](./reference.md)  ← loaded on demand
```

### Don't: Embed Everything
```markdown
# Overview
Brief intro.

## Full Reference
[500 lines of detailed documentation...]  ← wastes context
```

---

## Context Efficiency

### Do
- Link to supporting files
- Put scripts in `scripts/` directory (execute without loading source)
- Keep files modular and single-purpose

### Don't
- Embed large code blocks in SKILL.md
- Duplicate content across files
- Create deeply nested file structures

---

## Tool Restrictions (Optional)

Limit which tools Claude can use:

```yaml
---
name: read-only-analyzer
allowed-tools:
  - Read
  - Glob
  - Grep
---
```

---

## Troubleshooting

### Skill Doesn't Activate

1. Check description has specific trigger terms
2. Add "Use when..." clause
3. Test with explicit phrasing that matches description

### Too Much Context Used

1. Move detailed content to supporting files
2. Link instead of embed
3. Split large files into focused modules

### Skill Conflicts

1. Make descriptions more specific
2. Add distinguishing trigger terms
3. Consider merging related skills

---

## Anti-Patterns

| Anti-Pattern | Problem | Fix |
|--------------|---------|-----|
| Monolithic SKILL.md | Uses too much context upfront | Split into supporting files |
| Vague description | Never activates | Add specific action verbs and triggers |
| No quick reference | Forces full file load for simple tasks | Add concise quick-start section |
| Duplicate content | Wastes tokens, risks inconsistency | Single source of truth, link to it |

---

## Official Documentation

These practices are derived from official Claude Code documentation. When in doubt, check the source:

- [Claude Code Skills](https://code.claude.com/docs/en/skills) - Authoritative guide for Claude Code
- [Agent Skills Overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) - General Agent Skills docs
- [What are Skills?](https://support.claude.com/en/articles/12512176-what-are-skills) - Help Center explainer

Use `WebFetch` to pull latest docs if something isn't working as expected.
