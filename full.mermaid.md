---
title: "Service Blueprint: SaaS Customer Onboarding"
subtitle: "Comparing Self-Serve (SS) and Enterprise (EN) paths"
---

```mermaid
block-beta
  columns 7
  
  space:1 P1["1. SIGN UP →"]:1 P2["2. TRIAL →"]:1 P3["3. CONFIGURE ↔"]:1 P4["4. TRAIN →"]:1 P5["5. GO LIVE →"]:1 P6["6. SUPPORT"]:1
  
  TIME["⏱ TIME"]:1 T1["5min (SS)\n1-2wk (EN)"]:1 T2["14d (SS)\n30d (EN)"]:1 T3["1-3d (SS)\n2-4wk (EN)"]:1 T4["Self-paced (SS)\n1-2wk (EN)"]:1 T5["1 day"]:1 T6["Ongoing"]:1
  
  EV["EVIDENCE"]:1 E1["Landing page\nPricing\nContract (EN)"]:1 E2["Welcome email\nTrial dashboard\nSandbox"]:1 E3["Setup wizard (SS)\nConfig checklist (EN)\nIntegration docs"]:1 E4["Video tutorials (SS)\nTraining slides (EN)\nKnowledge base"]:1 E5["Production URL\nAdmin credentials\nLaunch checklist"]:1 E6["Help center\nStatus page\nInvoice"]:1
  
  CUST["CUSTOMER"]:1 C1["Visit website ★\nCreate account (SS)\nRequest demo (EN)"]:1 C2["Explore features ★\nImport sample data\nInvite teammates"]:1 C3["Follow wizard (SS)\nReview config (EN) ❗\nConnect integrations"]:1 C4["Watch videos (SS)\nAttend sessions (EN)\nComplete exercises"]:1 C5["Approve go-live ★\nMigrate data\nRoll out to users"]:1 C6["Submit tickets\nRequest features\nRenew subscription ★"]:1
  
  space:7
  LINE1["─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ line of interaction ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─"]:7
  space:7
  
  FRONT["FRONTSTAGE"]:1 F1["Welcome email ★\nSchedule demo (EN)\nAssign CSM (EN)"]:1 F2["Send tips email\nCheck-in call (EN)\nExtend trial (EN)"]:1 F3["In-app guidance (SS)\nConfig workshop (EN)\nReview settings (EN)"]:1 F4["Recommend content (SS)\nDeliver training (EN) ★\nCertify admins (EN)"]:1 F5["Confirm readiness\nMigrate production (EN)\nCelebrate launch ★"]:1 F6["Respond to tickets\nQBR meetings (EN)\nRenewal outreach"]:1
  
  space:7
  LINE2["─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ line of visibility ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─"]:7
  space:7
  
  BACK["BACKSTAGE"]:1 B1["Provision tenant\nLead scoring\nContract neg. (EN) ❗"]:1 B2["Track engagement\nScore health\nAlert on inactivity ❗"]:1 B3["Build integrations\nCustom config (EN) ❗\nSecurity review (EN)\nSSO setup (EN)"]:1 B4["Update LMS\nPrepare materials (EN)\nTrack completion ❗\nIssue certs (EN)"]:1 B5["Data migration (EN) ❗\nUAT validation (EN)\nCutover plan (EN)\nEnable billing"]:1 B6["Route tickets\nEscalate issues ❗\nChurn prediction\nGenerate invoice"]:1
  
  space:7
  LINE3["─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ internal interaction ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─"]:7
  space:7
  
  SUPP["SUPPORT"]:1 S1["Auth system\nTenant provisioning\nCRM integration"]:1 S2["Product analytics\nHealth scoring\nEmail automation"]:1 S3["Integration platform\nSSO/SCIM (EN)\nConfig management\nAudit logging"]:1 S4["LMS platform\nVideo hosting\nCertification engine\nCalendar booking"]:1 S5["Migration tooling\nRelease management\nBilling system\nMonitoring"]:1 S6["Ticketing system\nKnowledge base\nML churn model\nInvoicing"]:1

  style TIME fill:#f5f5f5,stroke:#999
  style EV fill:#f5f5f5,stroke:#999
  style CUST fill:#5a9aad,stroke:#2a6a7a,color:#fff
  style FRONT fill:#5a9aad,stroke:#2a6a7a,color:#fff
  style BACK fill:#5a9aad,stroke:#2a6a7a,color:#fff
  style SUPP fill:#5a9aad,stroke:#2a6a7a,color:#fff
  
  style T1 fill:#fff,stroke:#ccc
  style T2 fill:#fff,stroke:#ccc
  style T3 fill:#fff,stroke:#ccc
  style T4 fill:#fff,stroke:#ccc
  style T5 fill:#fff,stroke:#ccc
  style T6 fill:#fff,stroke:#ccc
  
  style E1 fill:#fafafa,stroke:#ccc
  style E2 fill:#fafafa,stroke:#ccc
  style E3 fill:#fafafa,stroke:#ccc
  style E4 fill:#fafafa,stroke:#ccc
  style E5 fill:#fafafa,stroke:#ccc
  style E6 fill:#fafafa,stroke:#ccc
  
  style C1 fill:#fff9e6,stroke:#c9a227
  style C2 fill:#fff9e6,stroke:#c9a227
  style C3 fill:#fff9e6,stroke:#c9a227
  style C4 fill:#fff9e6,stroke:#c9a227
  style C5 fill:#fff9e6,stroke:#c9a227
  style C6 fill:#fff9e6,stroke:#c9a227
  
  style F1 fill:#fff9e6,stroke:#c9a227
  style F2 fill:#fff9e6,stroke:#c9a227
  style F3 fill:#fff9e6,stroke:#c9a227
  style F4 fill:#fff9e6,stroke:#c9a227
  style F5 fill:#fff9e6,stroke:#c9a227
  style F6 fill:#fff9e6,stroke:#c9a227
  
  style B1 fill:#fff,stroke:#aaa
  style B2 fill:#fff,stroke:#aaa
  style B3 fill:#fff,stroke:#aaa
  style B4 fill:#fff,stroke:#aaa
  style B5 fill:#fff,stroke:#aaa
  style B6 fill:#fff,stroke:#aaa
  
  style S1 fill:#f3f3f3,stroke:#999
  style S2 fill:#f3f3f3,stroke:#999
  style S3 fill:#f3f3f3,stroke:#999
  style S4 fill:#f3f3f3,stroke:#999
  style S5 fill:#f3f3f3,stroke:#999
  style S6 fill:#f3f3f3,stroke:#999
  
  style LINE1 fill:none,stroke:none,color:#888
  style LINE2 fill:none,stroke:none,color:#888
  style LINE3 fill:none,stroke:none,color:#888
  
  style P1 fill:#e4f0f3,stroke:#5a9aad
  style P2 fill:#e4f0f3,stroke:#5a9aad
  style P3 fill:#e4f0f3,stroke:#5a9aad
  style P4 fill:#e4f0f3,stroke:#5a9aad
  style P5 fill:#e4f0f3,stroke:#5a9aad
  style P6 fill:#e4f0f3,stroke:#5a9aad
```

## Legend

| Symbol | Meaning |
|--------|---------|
| ★ | Moment of truth — customer perception crystallises |
| ❗ | Failure point — dependency or risk |
| → | One-way flow to next phase |
| ↔ | Negotiation / back-and-forth required |
| (SS) | Self-Serve path only |
| (EN) | Enterprise path only |

## Color Key

| Color | Lane |
|-------|------|
| Yellow (#fff9e6) | Customer-facing (Customer + Frontstage) |
| White (#fff) | Internal actions (Backstage) |
| Light grey (#f3f3f3) | Support systems |
| Very light grey (#fafafa) | Physical evidence |

## Notes

This blueprint compares two onboarding paths:
- **Self-Serve (SS)**: Fast, automated, self-paced
- **Enterprise (EN)**: Longer, high-touch, customised

Items without (SS) or (EN) suffix are common to both paths.
