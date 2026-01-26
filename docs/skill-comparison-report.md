# Comparison Report: Anthropic's `skill-creator` vs Our `skill-authoring`

## Overview

| Aspect | Anthropic's `skill-creator` | Our `skill-authoring` |
|--------|----------------------------|----------------------|
| **Name** | skill-creator | skill-authoring |
| **Focus** | Creating new skills | Creating AND evolving skills |
| **Structure** | SKILL.md + references/ + scripts/ | SKILL.md + supporting .md files |

---

## Structure Comparison

### Anthropic's skill-creator
```
skill-creator/
├── SKILL.md
├── LICENSE.txt
├── references/
│   ├── output-patterns.md
│   └── workflows.md
└── scripts/
    ├── init_skill.py
    ├── package_skill.py
    └── quick_validate.py
```

### Our skill-authoring
```
skill-authoring/
├── SKILL.md
├── structure.md
├── best-practices.md
└── evolution.md
```

---

## Content Comparison

### What Anthropic Covers That We Don't

| Topic | Details |
|-------|---------|
| **Output patterns** | Template pattern (strict vs flexible), examples pattern |
| **Workflow patterns** | Sequential workflows, conditional workflows |
| **Scripts** | `init_skill.py` for scaffolding, `package_skill.py` for distribution, `quick_validate.py` for validation |
| **Six-step creation process** | Understand → Plan → Initialize → Edit → Package → Iterate |
| **Bundled resources** | Detailed guidance on scripts/, references/, assets/ directories |
| **"Context window is a public good"** | Philosophy about token efficiency |

### What We Cover That Anthropic Doesn't

| Topic | Details |
|-------|---------|
| **Skill evolution** | Versioning, changelog patterns |
| **Updating from docs** | Workflow for checking/syncing with official docs |
| **Learning from experience** | Capturing session patterns as skill refinements |
| **Proactive recognition** | Signals for when to capture new patterns |
| **Session-end checklist** | Review prompts for skill refinement |
| **Anti-patterns table** | Monolithic SKILL.md, vague description, etc. |
| **Troubleshooting** | Skill doesn't activate, too much context, conflicts |

### Overlap (Both Cover)

- SKILL.md frontmatter (name, description required)
- Progressive disclosure principle
- File organization basics
- Keep SKILL.md under 500 lines
- Description importance for activation

---

## Philosophy Differences

| Anthropic | Ours |
|-----------|------|
| Focus on **creation** of new skills | Focus on **lifecycle** (create + evolve) |
| Provides **tooling** (Python scripts) | Provides **guidance** (markdown docs) |
| Emphasizes **bundled resources** | Emphasizes **learning patterns** |
| Production/enterprise oriented | Session-learning oriented |

---

## Gaps We Should Fill

### High Priority
1. **Output patterns** - How to structure skill outputs (templates vs examples)
2. **Workflow patterns** - Sequential and conditional workflow guidance
3. **Bundled resources** - Detailed guidance on scripts/, references/, assets/

### Medium Priority
4. **Initialization script** - Consider adding or referencing `init_skill.py`
5. **Validation** - Add validation checklist or reference official validator
6. **Six-step process** - Could adopt as a clearer creation workflow

### Low Priority (We Have Alternatives)
7. **Packaging** - Less relevant for project-local skills
8. **Licensing** - Only needed for public distribution

---

## Strengths of Our Approach

1. **Evolution focus** - Anthropic's skill is about creation; ours includes the full lifecycle
2. **Learning patterns** - Unique to us; not in Anthropic's skill
3. **Doc synchronization** - We have workflow for staying current with official docs
4. **Troubleshooting** - Practical debugging guidance
5. **Anti-patterns** - Clear "don't do this" guidance

---

## Recommendations

### Immediate Actions
1. Add `references/` directory with:
   - `output-patterns.md` (adapt from Anthropic's)
   - `workflow-patterns.md` (adapt from Anthropic's)
   - `bundled-resources.md` (new, based on Anthropic's guidance)

2. Update SKILL.md to mention:
   - Six-step creation process (reference to new file)
   - "Context window is a public good" philosophy

3. Add to best-practices.md:
   - Link to Anthropic's `init_skill.py` for scaffolding
   - Link to `quick_validate.py` for validation

### Keep As-Is (Our Unique Value)
- evolution.md - This is our differentiator
- Learning patterns section
- Session-end refinement checklist
- Troubleshooting section

---

## Sources

- [anthropics/skills repository](https://github.com/anthropics/skills)
- [skill-creator SKILL.md](https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md)
- [skill-creator/references/](https://github.com/anthropics/skills/tree/main/skills/skill-creator/references)
- [skill-creator/scripts/](https://github.com/anthropics/skills/tree/main/skills/skill-creator/scripts)
