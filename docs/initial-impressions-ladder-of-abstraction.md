# Initial Impressions: F1 Score Explainer as Ladder of Abstraction

*Captured: 2025-12-28*

## Core Concept

Following Bret Victor's "Up and Down the Ladder of Abstraction" - the explainer should let users move fluidly between levels of abstraction:

### The Ladder for F1 Score

```
ABSTRACT    All possible (Precision, Recall) pairs → F1 as a surface/contour
    ↕
MIDDLE      One threshold sweep → one PR curve, F1 varying along it
    ↕
CONCRETE    One threshold → one confusion matrix → one F1 value
```

## Key Interaction Patterns

1. **Linked representations**: Drag a point in precision-recall space → confusion matrix updates → formula highlights which terms change

2. **Parameter exploration**: "What if I had more false positives?" → slide a control → watch F1 respond in real-time

3. **Trajectory visualization**: Not just static points but paths - as threshold changes, trace the path through PR space

4. **Making the invisible visible**: Show things normally hidden, like harmonic mean's behavior vs arithmetic mean

## Design Qualities

- Immediate feedback (no "calculate" buttons)
- Dense information display
- Minimalist aesthetic, maximum clarity
- The visualization *is* the explanation

## Meta-Insight

The project itself is like a function: **inputs → outputs**

- Changing initial conditions/constraints has ripple effects downstream
- Need organization that makes these dependencies explicit
- When understanding evolves, we need to know what else must change

---

*This is a starting point to be refined as we import context from previous sessions.*
