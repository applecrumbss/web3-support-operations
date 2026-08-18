#  Triage Framework & Escalation Matrix

To maintain efficiency and protect user funds, all incoming tickets are triaged based on **Severity** and **Impact**.

---

## Triage Matrix

| Severity Level | Definition | Response Time (SLA) | Primary Handler |
| :--- | :--- | :--- | :--- |
| **P1 - Critical** | Exploits, smart contract bugs, widespread dApp downtime, active phishing attacks | < 15 Mins | Tier 3 Security / Engineering |
| **P2 - High** | Bridge delays > 6 hours, RPC node failures, repeated transaction reversions | < 1 Hour | Tier 2 Tech Ops |
| **P3 - Normal** | Wallet connection errors, gas estimation issues, missing token UI display | < 4 Hours | Tier 1 Support |
| **P4 - Low** | General inquiries, feature requests, documentation clarification | < 24 Hours | Tier 1 Support / Self-Serve KB |

---

## Escalation Workflow


[ Tier 1: Customer Support ]
│
├─► Resolved? ──► YES ──► Close Ticket & Update KB

│
└─► NO (Technical dApp/RPC Error) ──► Escalates to [ Tier 2: Tech Ops ]

│
└─► Vulnerability/Contract Bug? ──► [ Tier 3: Security / Eng ]

### Escalation Guidelines
1. **Tier 1 (Frontline Support):** Gathers TxHash, wallet address, chain ID, browser version, and console logs. Resolves standard UI, RPC, and setup issues.
2. **Tier 2 (Technical Operations):** Investigates RPC dropouts, stuck bridge relayers, and protocol indexing issues.
3. **Tier 3 (Security & Engineering):** Handles active exploit mitigations, contract paused states, and critical infrastructure bugs.
