# F1 Score: Ladder Mapping

How the Ladder of Abstraction applies specifically to our F1 Score explainer.

---

## The Ladder for F1 Score

| Level | View | Shows | Interaction |
|-------|------|-------|-------------|
| **Concrete** | Single confusion matrix | TP, FP, FN, TN → P, R → F1 | Adjust cell values directly |
| **Mid** | PR curve + F1 trace | One threshold sweep | Scrub threshold; see point move |
| **Abstract** | F1 surface over (P,R) space | All possible F1 values | Hover to see contours; click for instance |

---

## System Components for F1

| Component | What It Is | How to Abstract |
|-----------|------------|-----------------|
| **Independent Variable** | Classification threshold | Sweep threshold; show trajectory through PR space |
| **Structure** | F1 formula (harmonic mean of P and R) | Compare with arithmetic mean; show why harmonic |
| **Data** | Class distribution, model predictions | Sample different distributions; show effect on achievable F1 |

---

## Key Transitions to Support

| From | To | Interaction |
|------|-----|-------------|
| Confusion matrix | Point on PR curve | Change matrix → see point move |
| Point on PR curve | Confusion matrix | Click point → see example matrix |
| Point on PR curve | Region in F1 surface | Highlight corresponding contour |
| F1 surface location | Concrete example | Click anywhere → generate matching matrix |

---

## Key Insights the Ladder Should Enable

1. **Why harmonic mean?**
   - Concrete: See specific cases where arithmetic mean is misleading
   - Abstract: See how harmonic mean contours differ from arithmetic

2. **Precision-Recall tradeoff**
   - Concrete: Adjust threshold, watch P go up as R goes down
   - Abstract: See the full tradeoff curve all at once

3. **When F1 misleads**
   - Concrete: Find specific cases where high F1 hides problems
   - Abstract: See regions of F1 space that are "dangerous"

4. **Class imbalance effects**
   - Concrete: See one imbalanced example
   - Abstract: See how imbalance shifts the achievable region

---

## Evaluation Specifics for F1 Explainer

When evaluating F1 explainer components, check:

### Confusion Matrix View
- [ ] Can adjust TP, FP, FN, TN independently?
- [ ] Immediate P, R, F1 update?
- [ ] Constrained to valid values?

### PR Space View
- [ ] Shows current point?
- [ ] Shows threshold sweep trajectory?
- [ ] F1 contours visible?
- [ ] Can click to select point?

### Formula View
- [ ] Shows live calculation?
- [ ] Highlights which terms change?
- [ ] Compares harmonic vs arithmetic?

### Transitions
- [ ] Matrix ↔ PR point linked?
- [ ] Threshold slider ↔ both views?
- [ ] Hover shows values across views?
