# BPG Rental KPI — Run Log

## 2026-09-18 — KPI HOTFIX (marketSnap crash + ±5% bands + portfolio BM sum)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/  
**Stamp:** Sep 18, 2026 · 1:00 PM ET  

### Fixes
1. Guarded `marketSnap` (skip missing bands / null apartmentAvg / null YoY) — was throwing on `pr.bands['1'][0]` when `portRoyal.bands={}`, blanking market + dq + maint.
2. Beaufort bands → ±5% ranges (1BR `[1378,1522]` etc.). Port Royal BR bands populated (low-sample OK).
3. 828 B typed **Residence** + estBeds 3 so `800 Paris Ave (N)` market group paints.
4. `portfolioCollections.collected` = month-wise sum of entity BM sparks (Ember+Viktor+2203+BPG Rental+NNN). Documented in collectionsNote. Not Claude CSV SoT.
5. Skill/verification/data-shape: marketSnap + ±5% + portfolio definition locks.

### Proof
- marketSnap unit-test: Beaufort+PR rows, `$1,378–$1,522`, no null%.
- Paris residential comps: 4 (820B/824B/828B/832B).
- discrepancies 14, maintenance 10, Jan–Jul leftovers 0.


## 2026-09-18 — KPI FIX REBUILD (entity sparks + Jan–Aug labels + discrepancies)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim)  
**Stamp:** Sep 18, 2026 · 12:40 PM ET  
**Period:** Jan–Aug 2026 / as_of 2026-08-31  

### Fixes
1. `DATA.entities.*.inc` replaced flat monthly averages with live QBO cash P&L BM Month series (Ember/Viktor/2203 Total Income; Viktor + Other Income; BPG = Rental+NNN only).
2. All Jan–Jul / Jan&ndash;Jul UI leftovers → Jan–Aug / TYTLM through 2026-08-31 (grep = 0).
3. `DATA.discrepancies` expanded to 14 conflict rows (Miller closed, 67 Sams slip, vacancies, renewals, delinquency cured, entity-spark meta, BPG split gap).
4. Skill patched: entity `inc` must be true monthly BM series — never averages.

### API
- Live re-pull ProfitAndLoss Cash summarize_column_by=Month for ember/viktor/2203/bpg 2026-01-01→2026-08-31 — all OK.
- Property CF still Sep 11 TYTLM email CSVs (through Aug); entity CashFlow API present but property-by-customer CF not fully swapped this fix pass.
- No email CSV P&L fallback.

### Next run should
- Keep entity.inc from BM Month; assert len(set(inc))>1 (or document true flat).
- Prefer CashFlow API customer filters for property NI/cash when available.
- Confirm 25 Sams 2a signed term vs SREO; 137 Unit B co-tenant signature; 606 Unit 2 extension terms.


## 2026-09-18 — KPI FIX REBUILD (entity sparks + Jan–Aug labels + discrepancies)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim)  
**Stamp:** Sep 18, 2026 · 12:40 PM ET  
**Period:** Jan–Aug 2026 / as_of 2026-08-31  

### Fixes
1. `DATA.entities.*.inc` replaced flat monthly averages with live QBO cash P&L BM Month series (Ember/Viktor/2203 Total Income; Viktor + Other Income; BPG = Rental+NNN only).
2. All Jan–Jul / Jan&ndash;Jul UI leftovers → Jan–Aug / TYTLM through 2026-08-31 (grep = 0).
3. `DATA.discrepancies` expanded to 14 conflict rows (Miller closed, 67 Sams slip, vacancies, renewals, delinquency cured, entity-spark meta, BPG split gap).
4. Skill patched: entity `inc` must be true monthly BM series — never averages.

### API
- Live re-pull ProfitAndLoss Cash summarize_column_by=Month for ember/viktor/2203/bpg 2026-01-01→2026-08-31 — all OK.
- Property CF still Sep 11 TYTLM email CSVs (through Aug); entity CashFlow API present but property-by-customer CF not fully swapped this fix pass.
- No email CSV P&L fallback.

### Next run should
- Keep entity.inc from BM Month; assert len(set(inc))>1 (or document true flat).
- Prefer CashFlow API customer filters for property NI/cash when available.
- Confirm 25 Sams 2a signed term vs SREO; 137 Unit B co-tenant signature; 606 Unit 2 extension terms.



## 2026-09-18 — full monthly TEST RUN (Jan–Aug 2026 / as_of 2026-08-31)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim; dedicated `bpg-rental-kpi` still 404 / create blocked)  
**Stamp:** Sep 18, 2026 · 6:40 AM ET  
**Data period:** Jan–Aug 2026 (closed months) · QBO cash API primary

### Snapshot
- Occupancy: **31/34 (~91%)** after removing **27 Miller** (closed ~9/17). Vacant: 606 Unit 1, 606 Unit 2, 828 B.
- Collections: **~89.4%** of scheduled ($468,450 / $524,064) — **live QBO cash P&L Detail** (Customer-before-Name), NOT rent-roll proxy.
- Entity P&L BM reconcile: **TIED TO THE PENNY** for Ember / Viktor / 2203 / BPG.
- YTD property NI (CF CSVs, 16 props + Paris combined): reused Sep 11 TYTLM CF files (still through Aug).
- Below-market: Zumper Beaufort refreshed 2026-09-17 (median $2,100; BR bands studio/$1,125 · 1/$1,450 · 2/$1,838 · 3/$2,249 · 4/$2,600). RentCafe blocked.
- Under contract (kept): **67 Sams** — 9/18 close slipped; new 9/17 offer $385k / Nov close.
- Removed: **27 Miller** (closed ~9/17; wire confirmed).

### Conflicts printed
- Rent roll vs RUNNING vs Stinger: 606 Cottage occupied (lease 7/27); 828 B vacant post-reno; 25 Sams 2a renewing but signed extension unconfirmed; 820 B signed (was pending).
- 67 Sams: RUNNING said close 9/18 — Gmail shows new Nov offer (did not close).

### Open decisions
- 409 Carteret HVAC/ductwork ($12k + $6.5k)
- 828 B balcony door (ordered 8/21, ~9/18 arrive)
- 25 Sams 2a signed extension confirm
- 67 Sams sale response

### Sources
QBO thin API cash P&L Detail + BM (ember/viktor/2203/bpg) 2026-01-01→2026-08-31; property CF from Sep 11 TYTLM email CSVs; SREO xlsx; Projects Master RUNNING; Stinger vacancy Gmail; Zumper Beaufort/Port Royal.

### UI
- Template dashboard; savebar/LIVE disabled for Pages.
- No monthly email pack (test run).

---

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
