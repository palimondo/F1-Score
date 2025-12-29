# Skill Evolution

Skills are living documents. They should evolve as understanding deepens and patterns emerge.

---

## Versioning

### When to Version

- Major capability changes
- Breaking changes to structure or behavior
- Significant refinements from experience

### Simple Versioning Pattern

Add version to SKILL.md frontmatter:

```yaml
---
name: my-skill
description: ...
version: 1.2.0
last-updated: 2025-01-15
---
```

### Changelog Pattern

For skills that evolve frequently, add a changelog section or file:

```markdown
## Changelog

### v1.2.0 (2025-01-15)
- Added checklist for X based on session learnings
- Refined description triggers

### v1.1.0 (2025-01-10)
- Split reference.md into focused modules
```

---

## Updating from Official Docs

### When to Check

- Before major skill work
- When something doesn't work as expected
- Periodically (monthly?) for active skills

### Update Workflow

1. **Fetch current docs**:
   ```
   Use WebFetch on https://docs.anthropic.com/en/docs/claude-code/skills
   ```

2. **Compare with skill content**:
   - New features to incorporate?
   - Deprecated patterns to remove?
   - Changed best practices?

3. **Update and note**:
   ```markdown
   ## Changelog
   ### v1.3.0 (2025-01-20)
   - Updated per official docs refresh (new allowed-tools syntax)
   ```

### Key Doc URLs

| Topic | URL |
|-------|-----|
| Skills | https://docs.anthropic.com/en/docs/claude-code/skills |
| Memory | https://docs.anthropic.com/en/docs/claude-code/memory |
| Commands | https://docs.anthropic.com/en/docs/claude-code/slash-commands |

---

## Learning from Experience

### The Pattern

During a Claude Code session, effective patterns emerge through iteration. These should be captured before session context is lost.

### Recognition Signals

Claude (or user) should watch for:

1. **Repeated structure**: "We keep doing X the same way"
2. **Refined process**: "This worked better than our first approach"
3. **New checklist items**: "We should always check Y"
4. **Discovered anti-patterns**: "Z caused problems, avoid it"
5. **Effective prompts**: "When I phrase it this way, it works"

### Capture Workflow

1. **Identify the learning**:
   - What pattern emerged?
   - Why did it work?
   - What was the before/after?

2. **Locate the skill to update** (or create new):
   - Does this extend an existing skill?
   - Is it a new capability?

3. **Add with context**:
   ```markdown
   ### Pattern: [Name]

   **Discovered**: [session context]
   **Problem**: [what wasn't working]
   **Solution**: [what we found works]
   **Example**: [concrete usage]
   ```

4. **Commit with learning note**:
   ```
   git commit -m "Refine [skill]: add [pattern] from session learning"
   ```

---

## Proactive Learning Recognition

### For Claude

When you notice during a session:
- A workaround that became a pattern
- A question you answered that should be in a skill
- A checklist item that was missing
- An anti-pattern that caused problems

**Suggest to the user**:
> "We've developed an effective pattern for [X]. Should we capture this in the [skill-name] skill before we lose this context?"

### For Users

Prompt Claude with:
- "What have we learned in this session that should be captured?"
- "Does this pattern belong in a skill?"
- "Review our session for skill refinements"

---

## Skill Refinement Checklist

Before ending a significant session:

- [ ] Any new patterns worth capturing?
- [ ] Any checklist items discovered?
- [ ] Any anti-patterns to document?
- [ ] Any description triggers that didn't activate (but should)?
- [ ] Any supporting files that should be split or merged?

---

## Example: Evolving a Skill

### Original (v1.0)
```markdown
## Checklist
- [ ] Check A
- [ ] Check B
```

### After Session Learning (v1.1)
```markdown
## Checklist
- [ ] Check A
- [ ] Check B
- [ ] Check C ← Added: discovered this was missing when X failed

## Anti-Patterns
- Don't do Y before Z ← Learned the hard way
```

### After Docs Update (v1.2)
```markdown
## Checklist
- [ ] Check A (updated per docs: now includes A')
- [ ] Check B
- [ ] Check C

## Anti-Patterns
- Don't do Y before Z
- Avoid deprecated W pattern ← Removed from official docs
```
