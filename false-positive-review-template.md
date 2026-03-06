# False Positive Review Template

Document every confirmed false positive. This is the primary input to agent improvement.

---

## Case: [FRD-YYYY-XXXXXX]
## Date: [YYYY-MM-DD]
## Reviewer: [Name, Role]

---

## What Happened

**Action taken by agent:** Block / Step-up / Freeze / Other: ___

**Customer impact:**
- [ ] Transaction blocked — customer abandoned
- [ ] Transaction blocked — customer recovered via step-up
- [ ] Transaction blocked — customer called support
- [ ] Account frozen — customer contacted branch
- [ ] Other: ___

**Time to resolution:** ___ minutes / hours

**Customer sentiment (if known):** Neutral / Frustrated / Escalated / Churned

---

## Why the Agent Got It Wrong

**Risk score at time of block:** ___

**Signals that drove the false positive:**

| Signal | Value | Why It Was Misleading |
|---|---|---|
| | | |
| | | |

**Root cause:**
- [ ] Signal weight too high for this customer segment
- [ ] Customer behavior genuinely anomalous but legitimate (travel, large purchase, etc.)
- [ ] Missing context signal that would have resolved ambiguity
- [ ] Threshold too aggressive for this action type
- [ ] Model not updated to reflect customer's recent behavior change
- [ ] Other: ___

---

## What Should Change

**Recommended adjustment:**

| Component | Current Value | Recommended Value | Rationale |
|---|---|---|---|
| Signal weight: [signal name] | | | |
| Confidence threshold: [action] | | | |
| Customer segment exception | N/A | | |

**Risk of recommended change:**
- Estimated FP reduction: ___%
- Estimated FN increase: ___%
- Net expected impact: ___

**Approved by:** ___ **Date:** ___

---

## Pattern Tracking

Is this an isolated case or part of a pattern?

- [ ] Isolated
- [ ] Second occurrence — monitor
- [ ] Recurring pattern — threshold adjustment required
- [ ] Segment-level issue — requires model review

**Related cases:** FRD-___ · FRD-___ · FRD-___
