# Evaluation Checklists

Detailed criteria for evaluating ladder coverage.

---

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
| **Independent variable** | | | |
| **Structure** | | | |
| **Data** | | | |

---

## Open-Ended Evaluation Questions

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
