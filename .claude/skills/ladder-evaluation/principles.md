# Ladder of Abstraction: Core Principles

*Based on Bret Victor's essay: http://worrydream.com/LadderOfAbstraction/*

## The Problem Being Solved

> "How can we design systems when we don't know what we're doing?"

We're helping users develop intuition about systems where emergent behavior makes prediction difficult.

---

## The Three Moves

### Move 1: CONTROL (Develop Concrete Intuition)

**What it is:** Interactive adjustment of parameters to experience how the system behaves in specific cases.

**Requirements:**
- Direct manipulation of parameters
- Immediate feedback (no delays, no "calculate" buttons)
- Ability to move forward/backward through the independent variable
- Pause, jump, scrub through states
- Independent control of each parameter

**Purpose:** Build visceral, intuitive sense of "what happens when I do X"

---

### Move 2: ABSTRACT (See All Possibilities)

**What it is:** Representations that depict the system across *all* values of a parameter simultaneously.

**Techniques:**
- **Overlay/Trajectories**: Show multiple states superimposed
- **Small multiples**: Grid of examples varying one parameter
- **Coordinate transforms**: Reveal hidden structure
- **Summary metrics**: Compress behavior into comparable numbers
- **Contour maps/surfaces**: Show output across input space

**Conceptual operation:** Replace a concrete value with "*" (wildcard)

**Purpose:** See patterns that are invisible in any single instance

---

### Move 3: STEP DOWN (Ground the Abstract)

**What it is:** Return from abstract view to concrete instances to verify and explain.

**Requirements:**
- Point at abstract representation → access concrete state
- "Full stack" views showing ground level to abstract
- Maintain connection to visceral experience

**Key question:** "Does it make sense? Does it behave like we expect?"

**Purpose:** Verify abstract patterns with concrete evidence; prevent "stuck in the clouds"

---

## System Components

Every system has three components to address:

| Component | Description | How to Abstract Over It |
|-----------|-------------|------------------------|
| **Independent Variable** | The causality dimension (often time) | Show trajectories, animate, scrub |
| **Structure** | The rules/algorithm | Parameterize, show variations |
| **Data** | The input/environment | Sample space, show distributions |

---

## The Iteration Cycle

1. Choose one small, specific idea
2. Implement in the simplest manner possible
3. Explore up and down the ladder
4. Observe what happens
5. Get new ideas from observation
6. Repeat

### Three Outcomes of Good Exploration
1. **Intuitive understanding** (felt, not just known)
2. **Ideas for improvement** (grounded in observed behavior)
3. **Tools for rapid hypothesis testing** (can quickly check "what if")

---

## Anti-Patterns

| Anti-Pattern | Symptoms | Remedy |
|--------------|----------|--------|
| **Stuck on the ground** | Only concrete examples; no patterns visible; user must manually generalize | Add abstract views, overlays, or summaries |
| **Stuck in the clouds** | Only abstractions; lost touch with reality; can't verify claims | Add step-down interaction; click to see concrete |
| **Broken ladder** | Levels exist but transitions are jarring or missing | Add smooth interpolation; linked highlighting |
| **One-way ladder** | Can only go up OR down, not both | Ensure bidirectional: abstract↔concrete |
