# Agent Action Authority Template

Define the boundaries of autonomous agent action before deployment. Every action the agent can take must be explicitly authorized here. Actions not listed are not permitted.

**Agent:** [Agent Name]
**Version:** [v0.0]
**Date:** [YYYY-MM-DD]
**Approved by:** [Risk Officer] · [Legal] · [Product]

---

## Autonomous Action Register

Actions the agent may take without human approval:

| Action ID | Action | Trigger Condition | Min Confidence | Reversible? | Customer Notified? | Regulatory Flag |
|---|---|---|---|---|---|---|
| ACT-001 | Add step-up authentication | Risk score 31–60 | Moderate | Yes | Yes | None |
| ACT-002 | Delay real-time settlement | Risk score 61–85 | High | Yes (within window) | Yes | None |
| ACT-003 | Block single transaction | Risk score 86–100 | Critical | Partially | Yes | Reg E |
| ACT-004 | Notify customer of suspicious activity | Any fraud signal | Low | Yes | Yes | None |
| ACT-005 | Log for consortium sharing | Confirmed fraud pattern | High | No | No | BSA |

---

## Human-Required Action Register

Actions that require human approval before execution:

| Action ID | Action | Escalation SLA | Approver | Regulatory Flag |
|---|---|---|---|---|
| ACT-006 | Freeze account | 15 minutes | Fraud Ops Supervisor | Reg E |
| ACT-007 | File Suspicious Activity Report (SAR) | 24 hours | BSA Officer | BSA/AML |
| ACT-008 | Initiate account closure | 48 hours | Risk Officer + Legal | Multiple |
| ACT-009 | Block customer from channel | 30 minutes | Fraud Ops | Reg E |

---

## Prohibited Actions

Actions the agent is explicitly not permitted to take under any circumstances:

| Prohibited Action | Reason |
|---|---|
| Send funds to any destination | Fraud agents do not have payment authority |
| Access customer data outside fraud context | Data minimization principle |
| Communicate account closure to customer | Legal and regulatory process required |
| Make credit decisions | Separate model governance required |
| Share PII with external parties | Privacy and legal restrictions |

---

## Threshold Calibration Log

Document threshold changes over time:

| Date | Action | Previous Threshold | New Threshold | Reason | Approved by |
|---|---|---|---|---|---|
| YYYY-MM-DD | ACT-003 Block transaction | 90 | 86 | FP rate acceptable, FN rate too high | Risk Officer |

---

## Review Cadence

- **Monthly:** False positive and false negative rate review → threshold adjustment if needed
- **Quarterly:** Full action authority review with Risk, Legal, and Compliance
- **On model update:** Full re-validation before any threshold changes take effect

**Last reviewed:** [YYYY-MM-DD]
**Next review:** [YYYY-MM-DD]
**Signatures:** Risk Officer ___ · Legal ___ · Product ___
