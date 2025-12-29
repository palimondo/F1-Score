# Ladder of Abstraction: Principles & Evaluation Framework

*Based on Bret Victor's essay: http://worrydream.com/LadderOfAbstraction/*

---

## Part 1: Core Principles

### The Central Insight

> "The deepest insights are born not at any one level of abstraction, but in the **transitions between them**."

Understanding comes from the *dance* of moving up to see patterns, then down to explain them. A good explainer facilitates this dance.

### The Problem Being Solved

> "How can we design systems when we don't know what we're doing?"

We're helping users develop intuition about systems where emergent behavior makes prediction difficult. The goal is **intuitive understanding**, not just logical knowledge.

---

## Part 2: The Three Moves

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

## Part 3: System Components

Every system has three components to address:

| Component | Description | How to Abstract Over It |
|-----------|-------------|------------------------|
| **Independent Variable** | The causality dimension (often time) | Show trajectories, animate, scrub |
| **Structure** | The rules/algorithm | Parameterize, show variations |
| **Data** | The input/environment | Sample space, show distributions |

---

## Part 4: The Iteration Cycle

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

## Part 5: Anti-Patterns

| Anti-Pattern | Symptoms | Remedy |
|--------------|----------|--------|
| **Stuck on the ground** | Only concrete examples; no patterns visible; user must manually generalize | Add abstract views, overlays, or summaries |
| **Stuck in the clouds** | Only abstractions; lost touch with reality; can't verify claims | Add step-down interaction; click to see concrete |
| **Broken ladder** | Levels exist but transitions are jarring or missing | Add smooth interpolation; linked highlighting |
| **One-way ladder** | Can only go up OR down, not both | Ensure bidirectional: abstract↔concrete |

---

# Part 6: Evaluation Framework

## Checklist: Control (Concrete Level)

| Criterion | Question | Status |
|-----------|----------|--------|
| **Parameter access** | Can user manipulate each relevant parameter? | |
| **Immediacy** | Does feedback appear instantly (no button press, no delay)? | |
| **Reversibility** | Can user move backward as well as forward? | |
| **Scrubbing** | Can user smoothly drag through parameter space? | |
| **Independence** | Can each parameter be adjusted independently? | |
| **Starting point** | Is there a sensible default concrete example? | |

### Quality Gradient
- ❌ No interactivity (static)
- 🟡 Some interactivity but delayed or partial
- ✅ Full, immediate, reversible control

---

## Checklist: Abstract (Pattern Level)

| Criterion | Question | Status |
|-----------|----------|--------|
| **All-at-once view** | Is there a representation showing *all* values of some parameter? | |
| **Overlay/trajectory** | Can user see multiple states superimposed? | |
| **Summary metric** | Is there a number/visual that summarizes behavior? | |
| **Parameter space** | Is the space of possibilities made visible? | |
| **Pattern revelation** | Does the abstract view reveal something invisible in concrete? | |

### Quality Gradient
- ❌ No abstraction (only single examples)
- 🟡 Abstraction exists but doesn't reveal new patterns
- ✅ Abstraction reveals insights invisible at concrete level

---

## Checklist: Step Down (Grounding)

| Criterion | Question | Status |
|-----------|----------|--------|
| **Click-to-concrete** | Can user click on abstract view to see specific instance? | |
| **Hover preview** | Does hovering show concrete values? | |
| **Full stack visible** | Can user see concrete and abstract simultaneously? | |
| **Verification possible** | Can user check if abstract pattern holds for specific cases? | |
| **Return path** | After stepping down, can user easily return to abstract? | |

### Quality Gradient
- ❌ Abstract view is disconnected (can't access concrete from it)
- 🟡 Can step down but not smoothly or bidirectionally
- ✅ Fluid bidirectional movement; full stack visible

---

## Checklist: Transitions (The Key Test)

| Criterion | Question | Status |
|-----------|----------|--------|
| **Abstract → Concrete** | Click/select in abstract view → concrete instance appears? | |
| **Concrete → Abstract** | Drag/change concrete → see position in abstract space? | |
| **Linked highlighting** | Hovering one view highlights corresponding part in other? | |
| **Smooth interpolation** | Is movement between levels smooth, not jarring? | |
| **Insight emergence** | Do insights arise from moving between levels? | |

### Quality Gradient
- ❌ Levels are disconnected
- 🟡 Connection exists but in only one direction
- ✅ Bidirectional, smooth, insight-generating transitions

---

## Checklist: System Coverage

| Component | Abstracted Over? | Control Available? | Transitions Work? |
|-----------|------------------|-------------------|-------------------|
| **Independent variable** (e.g., threshold) | | | |
| **Structure** (e.g., F1 formula) | | | |
| **Data** (e.g., class distribution) | | | |

---

## Evaluation Questions (Open-Ended)

### For Each Prototype/Component:

1. **What level of abstraction does this operate at?**
   - Pure concrete? Pure abstract? Somewhere between?

2. **What can you NOT see from this view?**
   - What's hidden that another level would reveal?

3. **How do you get to adjacent levels?**
   - Is the path clear? Interactive? Smooth?

4. **What insight does this enable?**
   - Name a specific "aha" moment this facilitates

5. **What question can you answer here that you couldn't elsewhere?**
   - Each level should have unique value

### For the Overall Explainer:

6. **Can you trace a complete journey up and down?**
   - Start concrete → abstract fully → return to concrete

7. **Where does the ladder break?**
   - Identify gaps, dead ends, one-way streets

8. **Does the user understand MORE or just SEE more?**
   - Insight vs. information overload

---

## Quick Reference: The Ladder Applied to F1 Score

| Level | View | Shows | Interaction |
|-------|------|-------|-------------|
| **Concrete** | Single confusion matrix | TP, FP, FN, TN → P, R → F1 | Adjust cell values directly |
| **Mid** | PR curve + F1 trace | One threshold sweep | Scrub threshold; see point move |
| **Abstract** | F1 surface over (P,R) space | All possible F1 values | Hover to see contours; click for instance |

### Key Transitions to Support
- Confusion matrix ↔ Point on PR curve
- Point on PR curve ↔ Region in F1 surface
- Any abstract selection ↔ Concrete example with those values

---

*This framework should be used to evaluate prototypes and identify gaps in the ladder coverage.*
