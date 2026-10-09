# BPG Rental KPI — Run Log

## 2026-10-09 — FULL REBUILD Jan–Sep (Eric: entities reconciled thru Sep) — PUBLISHED

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/
**Stamp:** Oct 9, 2026 · 6:33 AM ET
**Period:** Jan–Sep 2026 / as_of 2026-09-30, ytdMonths=9. Live QBO cash (pulled 10/9, 0 API failures). identityGate.allPass=true; QA fails 0.

### Data-through (Oct 3 → Oct 9)
- Ember: 9/21 partial → books thru 10/7, Sep CLOSED (Sep int $8,566.06 + prin $2,503.38 posted on all 9 props).
- 2203: 9/8 partial → thru 10/2, Sep CLOSED (Lima One int $1,030.42 + prin $363.28).
- Viktor: 9/8 partial → entries thru 10/7 but Sep STILL PARTIAL: 609 Carteret + 409 Carteret Sep mortgage int/prin not posted.
- BPG: 10/3 → 10/9, complete. Ribaut excluded per portfolio lock.

### Restatements
- Sep entity NI: Ember $15,627 → −$5,012; 2203 $3,654 → $2,584; Viktor $9,145 → $5,068 (still partial); BPG $93,740 → $78,632.
- 153 Williams May/Jun interest back-posted ($252.26/$251.71).
- 67 Sams 433 Sep: +$500 other income (NI −$1,749.81 → −$1,249.81).

### Ops
- 606 U2 → OCCUPIED 9/5–11/30 (Jason Hurt furnished ST, $1,800) per Stephanie Chat 10/6 + SREO. Sep rent $0 on books → confirm Stinger disbursement. Occupancy 31/34.
- 828 B $2,250 confirmed (10/4 $1,750 was a typo). Balcony door swap Sat 10/10.
- SREO rent roll (updated 9/21): renewals 23WD A ($1,550), 137 B, 820 B, 25 Sams 2a; 820 A $1,802.50; 612 North DELINQUENT.
- 602 Battery turn WOs; 832 B plumbing Mon 10/12; 2203 803 Watkins invoice → SHM.

### Still not reconciled
Ember entity vs property income (Jan +$5,317.13, Feb −$4,700, Jun +$234.36, Jul +$3,000); 23 White Dogwood Sep (−$1,512.50); 609 parent income vs units (~$512–536/mo Jan, Mar–Aug); 828 B $2,250/mo collected Jan–Aug while vacant; 67 Sams HomeSpring ~$33.4K Jan–Aug on parent 430; Viktor Sep mortgages (609/409); 606 U2 Sep rent.

### Next run should
- Re-check Viktor Sep (609/409) and drop Viktor † once posted.
- Dual T&I run-rate (deferred again). Drive RUNLOG/CONTEXT docs not updated this run (repo RUNLOG only).

---

## 2026-10-05 — Weekly partial (ops-only, Monday) — BUILT, PUBLISH BLOCKED

**Target:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (live still shows Oct 3, 2026 · 11:44 AM ET full rebuild)
**Stamp (built):** Oct 5, 2026 · 9:58 AM ET. Local commit (HEAD, ahead 1) in /workspace/bpg-tasks-publish (ahead 1, NOT pushed: GH_TOKEN empty in routine shell).
**Base:** Oct 3 full rebuild (Jan–Sep, live QBO). No QBO re-pull. Dual T&I deferred to 12th.

### Material
1. **606 Carteret Unit 2** — Stephanie 10/4 prospect email: furnished, available end Nov / early Dec, $1,800 (board: vacant since 8/31, $1,850). Kept Vacant (no lease evidence); ask → $1,800; conflict printed.
2. **828 B** — Stephanie 10/4 email quoted $1,750; Stinger listing still $2,250 on 10/5. Kept $2,250; conflict printed. Austin 10/4 questioned Masi credit.
3. New lead Beth Hartle (10/4) for 606 U1 / U2 / 828 B, CC Stinger leasing.

### Not material
- 409 Carteret refi inquiry (Futures Funding, call Wed 10/7) is financing, not board ops.
- RUNNING last modified 10/3 2:39 AM ET (already in Oct 3 build). No Stinger mail since 10/3. Occupancy 30/34 unchanged.

### Next run should
- Push the local HEAD commit (or rebuild from /workspace/rental-kpi/wk1005) once GH_TOKEN is available.
- Resolve 606 U2 status (occupied/held through Nov?) and 828 B asking rent.
- 67 Sams DD ends Oct 9; close Oct 29.
- Monthly 12th: full QBO + dual T&I run-rate.

---

## 2026-10-03 — Full rebuild (Jan–Sep 2026, live QBO cash)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim; dedicated `bpg-rental-kpi` still not available to the PAT)
**Scope:** Full rebuild: QBO cash P&L BM + P&L Detail (Customer) + CashFlow per customer, Jan 1–Sep 30; Chat REST + RUNNING (Oct 3) + Gmail + Gemini notes for ops. ytdMonths=9. Dual T&I run-rate DEFERRED.

### Data-through (Sep is PARTIAL where books are behind)
- **Ember:** books end 9/21 (last P&L txn 9/18); Sep mortgage interest + principal NOT posted; Sep income $20.6K vs ~$26.7K normal. NOT current.
- **Viktor:** books end 9/8 (no Sep interest on 609 / 409; OpEx light). **2203:** ends 9/8 (no Sep interest/principal). **BPG:** current 10/3.
- Page shows per-entity "books thru" chips, an amber banner, † on Sep columns/flags, and a "Jan–Aug final" line on partial entity cards.

### Changes vs 9/28 board
- Rollover to Jan–Sep; Ember Jun restated (+$765.11: 1122 Emmons +$518.25, 602 Battery +$12.50, unattributed +$234.36).
- 2203 Actual CF now NI − principal (was net-cash-increase w/ bridge rows). Paris DSCR window now Apr–Sep.
- 67 Sams (cust 433): Sep NI −$1,749.81 incl. $4,311.10 HomeSpring interest (Jan–Aug HomeSpring ~$33K still on parent 430 — allocation inconsistency flagged).
- 27 Miller $405K sale posted to cust 431 in Sep (excluded). Market overall medians refreshed 10/3 (Zumper); BR bands carried from 9/18.
- Ops: 828 B door delivered 9/30; 602 Battery inspection done; 606 U1 128 DOM; 409 HVAC Watkins $9,300 vs Lang; Cottage WO #115751; Calie left Stinger 10/2.

### Did not reconcile
Ember entity-vs-property income residuals (Jan +5,317.13, Feb −4,700, Jun +234.36, Jul +3,000); 23 White Dogwood Sep (−$1,512.50); 609 Carteret parent-level income ~$512–536/mo Jan–Aug; 828 B collected $2,250/mo Jan–Aug while vacant; missing Sep mortgage postings (Ember, 2203, 609, 409).

## 2026-09-28 — Weekly partial (ops-only, Monday)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim; dedicated `bpg-rental-kpi` may still be PAT-blocked)  
**Stamp:** Sep 28, 2026 · 10:05 AM ET  
**Scope:** Chat + RUNNING + Stinger/Gmail only. No QBO rebuild. Dual T&I deferred to 12th.

### Material
1. **602 Battery Ln** — **Vacant** (tenant moved out 9/23; Chat move-out report 9/25; RUNNING inspection Oct 2). Was occupied through 9/30 / not renewing.
2. **606 Carteret Unit 1** — asking rent **$1,750** (RUNNING Calie 9/24; was $1,800 on 9/21 board). Still vacant / listed.
3. **67 Sams Point Rd** — Dawn backup promoted to primary 9/22 (Greco). **DD Oct 9 · close Oct 29** (was DD 10/16 / Nov on prior board).
4. **153 Williams** — sewer/drain WO #115458 ~$4,250 **approved** 9/25 (Eric verbal) — added to open maint.
5. **828 B** — Kimberly Masi lead (missed 9/25 showing → SHM); balcony door still unconfirmed. Still vacant @ $2,250.
6. **137 Old Jericho** — tree trim (Karr ~9/23) added; Unit B co-tenant signature still unconfirmed.
7. **606 Unit 2** — status field reconciled to Vacant (lease ended 8/31; already in vacant count).

### Occupancy
**30/34 (~88%)** — vacant: 606 U1, 606 U2, 828 B, 602 Battery.

### Conflicts printed
- 606 U1 asking: Chat 9/17 $1,800 vs RUNNING 9/24 $1,750 → preferred RUNNING.
- 67 Sams timeline: board Nov/10/16 vs Greco 9/22 Oct 9/Oct 29 → preferred Greco + calendar + RUNNING.
- 602 Battery: lease-end 9/30 on board vs moved-out 9/23 Chat/RUNNING → preferred Chat/RUNNING.

### Not material / unchanged
- 23 White Dogwood B extension still SIGNED.
- 25 Sams 2a signed extension still unconfirmed.
- 409 HVAC decision still open.
- 27 Miller remains excluded (closed).
- Routine WOs (2203 803 freon, 2905 Second leak, stove/washer estimates) not board decisions.

### Sources
Chat REST OK (secret-backups OAuth). RUNNING Drive doc OK. Gmail Stinger/Rentvine/Greco OK.

### Next run should
- Confirm 828 B door received/installed; Masi/SHM application outcome.
- Confirm 25 Sams 2a + 137 B signatures.
- 602 Battery turn complete → list.
- Monthly 12th: full QBO + dual T&I run-rate.

---

## 2026-09-21 — Weekly partial (ops-only, Monday)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/ (interim; dedicated `bpg-rental-kpi` still PAT 404)  
**Stamp:** Sep 21, 2026 · 10:30 AM ET  
**Scope:** Chat + RUNNING + Stinger/Gmail only. No QBO rebuild. Dual T&I deferred to 12th.

### Material
1. **23 White Dogwood Unit B** — lease extension **SIGNED** (Stephanie Chat 9/17; RUNNING). Was “renewing / signature pending.” ≤90d rail → ok.
2. **606 Carteret Unit 1** — asking rent **$1,800** (was $1,850; Chat 9/17). Still Vacant / listed (MLS via TGG 9/17). No occupancy flip.

### Not material / unchanged
- Vacants unchanged: 606 Unit 1, 606 Unit 2, 828 B.
- 27 Miller already removed (closed ~9/17).
- 67 Sams still under contract (Dawn $385k / Nov) — no new path this week.
- 25 Sams 2a / 137 Unit B signatures still unconfirmed.
- 828 B balcony door: ETA ~9/18 passed; receipt/install unconfirmed — left open.
- WO 115508 (2203 quarterly pest) = routine; not board decision.
- 609 electric WO: Carmen closing (no tenant contact) — not on open-decision list.

### Sources
Chat REST OK (OAuth refresh from secret-backups). RUNNING Drive doc OK. Gmail Stinger/Rentvine OK.

### Next run should
- Confirm 828 B balcony door received/installed.
- Confirm 25 Sams 2a + 137 B signatures.
- Monthly 12th: full QBO + dual T&I run-rate.

---

## 2026-09-18 — Eric feedback fix (DSCR, Actual CF, below-market, tiles)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/  
**Stamp:** Sep 18, 2026 · 2:49 PM ET  

### Fixes
1. Below-market: `renderEntityCards()` runs **after** comps; entity below sums to portfolio 17 (Ember 8 + Viktor 7 + 2203 2).
2. Removed redundant Rental units / Occupied tiles (subheader keeps props·units·occ).
3. DSCR = (NI + interest add-back) ÷ (scheduled P&I × months). Ember ~1.34 (was 0.65 from post-interest NI ÷ inflated debtSvc).
4. Actual CF/mo = NI − principal (after P&I). 2203 uses entity cash increase (~$1,571/mo, was $3,954). Paris cleanCash Mar–Aug after P&I ~$1,776 (was −$4,584 raw net-cash w/ capex).
5. Viktor/Paris NI counted once via parisGroup.


## 2026-09-18 — FULL RERUN (API customer CF + By-Entity UI)

**Live:** https://bermanpropertygroup.github.io/bpg-tasks/rental-kpi/  
**Stamp:** Sep 18, 2026 · 1:18 PM ET  
**Period:** Jan–Aug 2026 / as_of 2026-08-31  

### Data
- Live QBO: entity P&L BM + CashFlow BM + ProfitAndLossDetail (all 4 companies) — OK.
- Per-customer CashFlow BM Month for 17 property customers (ember/viktor/2203/bpg) — **0 errors**. Sample: Ember 153 Williams cust=4; Viktor 800 Paris cust=10; BPG 67 Sams cust=433; 2203 cust=1; 3B/3D cust=16/17.
- Property `actNi`/`actCash` from API CF (Net Income / Net cash increase). **No Sep-11 email CSV** for property CF.
- Entity sparks still true BM monthly series; portfolioCollections = Σ sparks.
- 27 Miller excluded; market ±5% bands + marketSnap guard retained.

### UI
- By Entity cards: snapshot metric grid (units, occ, expected, NI, CF, DSCR, below-market) + spark.
- Open items / Recently completed / property table: entity expand/collapse headers.
- Template `templates/dashboard.html` synced from published board.

### Next run should
- Keep customer CF BM primary; never reintroduce email CF while API succeeds.
- Confirm 828 B baths with Eric; keep Residence type.

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
