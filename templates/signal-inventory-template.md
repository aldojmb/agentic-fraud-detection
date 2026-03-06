# Signal Inventory Template

Map all available signals before designing your fraud detection agent. Signals you don't inventory don't get used.

---

## Agent: [Agent Name]
## Fraud Type: [Transactional / ATO / Synthetic Identity / Other]
## Date: [YYYY-MM-DD]
## Owner: [PM Name]

---

## Signal Inventory

For each available signal, document:

| Signal ID | Signal Name | Source System | Latency | Availability | Fraud Pattern |
|---|---|---|---|---|---|
| SIG-001 | | | ms / s / min | Real-time / Batch | ATO / Transactional / SIF |
| SIG-002 | | | | | |

---

## Signal Categories

### Behavioral Signals
| Signal | Source | Latency | Notes |
|---|---|---|---|
| Session typing cadence | Browser/App SDK | <50ms | |
| Navigation flow deviation | App analytics | <100ms | |
| Device orientation/interaction | Mobile SDK | <100ms | |

### Device Signals
| Signal | Source | Latency | Notes |
|---|---|---|---|
| Device fingerprint | Device intelligence | <50ms | |
| New device flag | Auth system | <50ms | |
| Rooted/jailbroken | Mobile SDK | <50ms | |
| Emulator detected | Device intelligence | <50ms | |

### Network Signals
| Signal | Source | Latency | Notes |
|---|---|---|---|
| IP geolocation | IP intelligence | <100ms | |
| IP reputation | Threat intel feed | <100ms | |
| VPN/Proxy/Tor flag | IP intelligence | <100ms | |
| Distance from last known IP | Auth system | <100ms | |

### Transaction Signals
| Signal | Source | Latency | Notes |
|---|---|---|---|
| Amount vs 90-day average | Core banking | <200ms | |
| New beneficiary flag | Payments system | <50ms | |
| Time since beneficiary added | Payments system | <50ms | |
| Channel vs usual pattern | Auth system | <100ms | |

### Account History Signals
| Signal | Source | Latency | Notes |
|---|---|---|---|
| Recent profile changes | CRM | <200ms | |
| Failed authentication count (24h) | Auth system | <100ms | |
| Recent limit increase requests | Core banking | <200ms | |
| Linked account changes | Core banking | <200ms | |

### External Signals
| Signal | Source | Latency | Notes |
|---|---|---|---|
| Consortium fraud feed | Industry network | <500ms | |
| Mule account indicators | Fraud ops database | <200ms | |
| Threat intelligence | External feed | <500ms | |

---

## Signal Gap Analysis

Signals you need but don't have access to:

| Signal | Why Needed | Gap Type | Resolution Path |
|---|---|---|---|
| | | Missing source / Latency too high / Not integrated | |

---

## Signal Weight Assumptions

Initial weight assumptions before calibration (adjust after model validation):

| Signal Category | Initial Weight Range | Rationale |
|---|---|---|
| Behavioral | 0.10 – 0.20 | Strong for ATO, weaker for transactional |
| Device | 0.15 – 0.35 | High weight for new/anomalous device |
| Network | 0.10 – 0.25 | Context-dependent |
| Transaction | 0.20 – 0.40 | Core signal for transactional fraud |
| Account history | 0.15 – 0.30 | High weight for ATO stage detection |
| External | 0.10 – 0.20 | High precision, lower coverage |

*Weights must be validated against labeled fraud data before production deployment.*
