# Contributing to Agentic Fraud Detection Patterns

This repo documents architecture patterns from production fraud detection systems. Contributions grounded in real deployment experience are welcome.

---

## What kinds of contributions are useful

**New detection patterns**
Additional fraud patterns not covered (friendly fraud, first-party fraud, APP scams, crypto fraud) with signal inventories and agent reasoning flows based on real cases.

**Signal additions**
New signals for existing patterns — particularly open banking signals, alternative data sources, or behavioral biometrics that have proven effective in production.

**Regulatory additions**
Fraud-specific regulatory requirements for jurisdictions not currently covered (EU PSD2, UK APP fraud reimbursement rules, RBI guidelines, etc.).

**Calibration data**
Anonymized or synthesized threshold calibration data that helps practitioners set initial confidence thresholds for their context.

**False positive patterns**
Common false positive scenarios with resolution approaches — this is the most underrepresented knowledge in public fraud detection literature.

---

## What to avoid

- Patterns based on synthetic or demo scenarios without production validation
- Signal descriptions that reveal specific vendor implementations in ways that could help fraudsters adapt
- Regulatory references that have not been verified as current

---

## How to contribute

1. Fork the repo
2. Create a branch: `git checkout -b your-contribution-name`
3. Make your changes
4. Open a pull request with context on the production environment (anonymized) where the pattern was observed

---

## Citation

```
Macías, Aldo J. (2025). Agentic Fraud Detection Patterns.
https://github.com/aldojmb/agentic-fraud-detection
```

---

## Contact

Aldo J. Macías — [linkedin.com/in/aldojmacias](https://linkedin.com/in/aldojmacias) · [aldojm.com](https://aldojm.com)
