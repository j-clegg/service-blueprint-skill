---
title: "Service Blueprint: Coffee Shop Order"
---

```mermaid
block-beta
  columns 4
  
  space:1 P1["1. ORDER →"]:1 P2["2. PREPARE →"]:1 P3["3. DELIVER"]:1
  
  TIME["⏱ TIME"]:1 T1["1-2 min"]:1 T2["3-5 min"]:1 T3["30 sec"]:1
  
  EV["EVIDENCE"]:1 E1["Menu board\nPOS terminal"]:1 E2["Order ticket\nCoffee machine"]:1 E3["Branded cup\nReceipt"]:1
  
  CUST["CUSTOMER"]:1 C1["Review menu ★\nPlace order\nPay"]:1 C2["Wait"]:1 C3["Collect drink ★\nLeave"]:1
  
  space:4
  LINE1["─ ─ ─ ─ ─ ─ ─ line of interaction ─ ─ ─ ─ ─ ─ ─"]:4
  space:4
  
  FRONT["FRONTSTAGE"]:1 F1["Greet customer ★\nTake order\nProcess payment"]:1 F2["Call name\nwhen ready"]:1 F3["Hand over drink\nThank customer"]:1
  
  space:4
  LINE2["─ ─ ─ ─ ─ ─ ─ line of visibility ─ ─ ─ ─ ─ ─ ─"]:4
  space:4
  
  BACK["BACKSTAGE"]:1 B1["Print ticket"]:1 B2["Pull espresso ❗\nSteam milk\nAssemble drink"]:1 B3["Quality check"]:1
  
  space:4
  LINE3["─ ─ ─ ─ ─ ─ internal interaction ─ ─ ─ ─ ─ ─"]:4
  space:4
  
  SUPP["SUPPORT"]:1 S1["POS system\nPayment gateway"]:1 S2["Coffee machine\nBean supply ❗"]:1 S3["Cup inventory"]:1

  style TIME fill:#f5f5f5,stroke:#999
  style EV fill:#f5f5f5,stroke:#999
  style CUST fill:#5a9aad,stroke:#2a6a7a,color:#fff
  style FRONT fill:#5a9aad,stroke:#2a6a7a,color:#fff
  style BACK fill:#5a9aad,stroke:#2a6a7a,color:#fff
  style SUPP fill:#5a9aad,stroke:#2a6a7a,color:#fff
  
  style T1 fill:#fff,stroke:#ccc
  style T2 fill:#fff,stroke:#ccc
  style T3 fill:#fff,stroke:#ccc
  
  style E1 fill:#fafafa,stroke:#ccc
  style E2 fill:#fafafa,stroke:#ccc
  style E3 fill:#fafafa,stroke:#ccc
  
  style C1 fill:#fff9e6,stroke:#c9a227
  style C2 fill:#fff9e6,stroke:#c9a227
  style C3 fill:#fff9e6,stroke:#c9a227
  
  style F1 fill:#fff9e6,stroke:#c9a227
  style F2 fill:#fff9e6,stroke:#c9a227
  style F3 fill:#fff9e6,stroke:#c9a227
  
  style B1 fill:#fff,stroke:#aaa
  style B2 fill:#fff,stroke:#aaa
  style B3 fill:#fff,stroke:#aaa
  
  style S1 fill:#f3f3f3,stroke:#999
  style S2 fill:#f3f3f3,stroke:#999
  style S3 fill:#f3f3f3,stroke:#999
  
  style LINE1 fill:none,stroke:none,color:#888
  style LINE2 fill:none,stroke:none,color:#888
  style LINE3 fill:none,stroke:none,color:#888
  
  style P1 fill:#e4f0f3,stroke:#5a9aad
  style P2 fill:#e4f0f3,stroke:#5a9aad
  style P3 fill:#e4f0f3,stroke:#5a9aad
```

## Legend

| Symbol | Meaning |
|--------|---------|
| ★ | Moment of truth — customer perception crystallises |
| ❗ | Failure point — dependency or risk |
| → | Flow to next phase |

## Notes

- **Yellow boxes**: Customer-facing actions (customer + frontstage)
- **White boxes**: Internal actions (backstage)
- **Grey boxes**: Support systems
