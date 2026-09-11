# BPG Rental KPI Dashboard

Read-only portfolio KPI dashboard for Berman Property Group rentals.

**Live:** https://bermanpropertygroup.github.io/bpg-rental-kpi/

## Scope
- 21 rental properties / 35 units across Ember Invest, Viktor Group, 2203 First Blvd 800 LLC, BPG LLC commercial
- Excludes 1827 Ribaut (storage) and 614 Prince (lot)
- 27 Miller / 67 Sams kept while under contract (remove only after close)

## Data
Report-based (no live QBO connector). Monthly COO run pulls:
1. Gmail QBO CF_TYTLM / StmtCF CSVs (`02 Accounting/QBO Reports`)
2. SREO workbook (debt service, proforma DSCR, rent roll)
3. Projects Master RUNNING / DISPOSITION (status, maintenance)
4. Ember_QBO_Sync sheet (Ember gaps)

Status/notes edits happen in Projects Master / Chat — not on this static page.

## Publish
`index.html` on `main` → GitHub Pages (root).
