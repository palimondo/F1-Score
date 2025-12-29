# Skill File Structure

## Location Options

| Location | Path | Scope |
|----------|------|-------|
| Project | `.claude/skills/` | Repository collaborators |
| Personal | `~/.claude/skills/` | Individual user only |
| Enterprise | Platform-managed | Organization-wide |

## Single-File Skill

For simple skills:

```
.claude/skills/
└── simple-skill/
    └── SKILL.md
```

## Multi-File Skill (Recommended)

For complex skills with progressive loading:

```
.claude/skills/
└── complex-skill/
    ├── SKILL.md           # Entry point (overview, quick ref)
    ├── reference.md       # Detailed documentation
    ├── examples.md        # Usage examples
    ├── checklist.md       # Evaluation criteria
    └── scripts/           # Utility executables
        └── helper.sh
```

## Context Loading Stages

### Stage 1: Discovery (Startup)
- Only skill names and descriptions loaded
- Fast startup, minimal context

### Stage 2: Activation (Matching)
- Full `SKILL.md` loads when request matches description
- Supporting file names visible

### Stage 3: Execution (On Demand)
- Supporting files load only when Claude needs them
- Scripts execute without loading source into context

## File Size Guidelines

| File | Recommended Max |
|------|-----------------|
| SKILL.md | 500 lines |
| Supporting files | 300 lines each |
| Total skill | Keep modular, not monolithic |

## Linking Pattern

In SKILL.md, link to supporting files:

```markdown
## More Details

- [Full API Reference](./reference.md)
- [Usage Examples](./examples.md)
```

Claude reads these only when the task requires deeper detail.
