# BPG Rental KPI — Run Log

## 2026-09-13 — site-UI rebuild (Jan–Aug 2026 / Sep 11 numbers)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim; dedicated `bpg-rental-kpi` create still blocked by PAT)  
**Stamp:** Sep 13, 2026 · 11:12 AM ET  
**Data period:** Jan–Aug 2026 (closed months from Sep 11 TYTLM push)

### Snapshot
- Occupancy: **33/35 (94%)** — 606 Unit 1 vacant; 828B vacant
- Collections: **87%** rent-roll PROXY ($454,338 / $523,819) — *not* QBO cash receipts
- YTD Net Income (CF props): **$44,281** (16 property CSVs; Miller/Sams missing CF)
- Open maintenance / decisions: **10**
- Below-market: template market bands as-of **Aug 23, 2026** (comps not refreshed Sep 11)
- Under contract (kept): **27 Miller**, **67 Sams** — not closed as of 2026-09-11

### UI
- Rebuilt from canonical site template (`templates/dashboard.html`) — attention rails, entity group toggle, market band, collections + NI/cash charts, expandable units, open items.
- Savebar / LIVE overlays **disabled** for public Pages (`#savebar` forced `display:none`; `markDirty` no-op; edit buttons hidden). No `localStorage`.

### Gaps (unchanged)
- No unit-level P&L TxDetail parse this period
- No CF for 27 Miller / 67 Sams
- Market comps not refreshed Sep 11 / Sep 13

---

## 2026-09-11 — v5 (Jan–Aug 2026 / TYTLM Sep push)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim; dedicated repo create blocked by PAT)  
**Commit (bpg-tasks):** `08218427741848b8f8af0cf4dcf463626a85d2a0`  
**Stamp:** Sep 11, 2026 (ET)  
**Data period:** Jan–Aug 2026

### Snapshot
- Occupancy: **33/35 (94%)** — RUNNING-reconciled (606 Unit 1 vacant; 828B vacant; Emmons STR active)
- Collections: **87%** rent-roll proxy ($454,338 / $523,819) — *not* QBO cash receipts this run
- YTD Net Income (CF props): **~$44,281** (16 property CSVs; Miller/Sams missing CF)
- Open maintenance / decisions: 10 open+decision items
- Under contract (kept): **27 Miller**, **67 Sams** — not closed as of 2026-09-11 (target ~9/18)

### Open decisions
- 409 Carteret HVAC/ductwork ($12k + $6.5k)
- 828 B balcony door (ordered 8/21, ~9/18 arrive)

### Gaps
- No unit-level P&L TxDetail parse (collections = rent-roll proxy)
- No CF for 27 Miller / 67 Sams
- Ember_QBO_Sync Aug rental income blank at entity level
- Drive fallback folder empty
- Below-market gap TBD (comps not refreshed; v4 ~$3,484/mo)

### Sources
Gmail CF_TYTLM Sep 11 ~07:00 ET + Ember StmtCF; SREO; Projects Master RUNNING; Ember_QBO_Sync.

---
*(Paste into Drive runlog doc 1f1igpJyefgpqb0Ta8YopJWwuJMvVv89Kn2tzivD2TTw — Drive MCP cannot append Doc body.)*
