# 06 – Operational Losses

> **Last Reviewed:** 2026-06-28
> **Owner:** Production Manager / Continuous Improvement Lead

---

## Contents

1. [Loss Framework Overview](#1-loss-framework-overview)
2. [OEE Breakdown](#2-oee-breakdown)
3. [Loss Categories and Definitions](#3-loss-categories-and-definitions)
4. [OEE Data by Line](#4-oee-data-by-line)
5. [Top Losses Analysis (Pareto)](#5-top-losses-analysis-pareto)
6. [Root Cause Analysis](#6-root-cause-analysis)

---

## 1. Loss Framework Overview

BKK uses the **Overall Equipment Effectiveness (OEE)** framework to measure and manage operational losses. OEE is calculated as:

```
OEE = Availability × Performance × Quality

Where:
  Availability  = (Planned Production Time − Unplanned Downtime) / Planned Production Time
  Performance   = (Actual Output × Ideal Cycle Time) / Run Time
  Quality       = Good Units Produced / Total Units Started
```

In addition to OEE, BKK tracks **material losses** (yield loss, waste, and rework) separately, as these impact both cost and environmental performance.

### Loss Categories — Top Level

| Loss Type | Measured By | Captured In |
|---|---|---|
| Availability losses | Unplanned downtime minutes | Line logbook / SAP PM notifications |
| Performance losses | Speed loss (units below rated rate) | Line logbook / MES (where available) |
| Quality losses | Defects, rejects, rework at filling/packing | SAP QM / Quality log |
| Material (yield) losses | Bulk loss, filling overfill, cleaning losses | SAP PP batch records / QA yield report |

---

## 2. OEE Breakdown

### OEE Waterfall (Illustrative)

```
Planned Production Time (PPT)                 = 100%
  Less: Planned Stoppages (maintenance, CIP)  =  -X%
────────────────────────────────────────────────────
Available Time                                = A%

  Less: Unplanned Downtime                    =  -X%
────────────────────────────────────────────────────
Run Time                                      = A × Avail%

  Speed Loss (actual rate < rated rate)       =  -X%
────────────────────────────────────────────────────
Net Operating Time (at rated speed)           = A × Avail% × Perf%

  Quality Loss (defects, rework, rejects)     =  -X%
────────────────────────────────────────────────────
OEE                                           = A × Avail% × Perf% × Qual%
```

> **Note:** Planned stoppages (e.g., scheduled changeovers, planned maintenance) are excluded from OEE's Availability calculation but are tracked separately as **Planned Downtime Losses** because they represent recoverable time through programmes like SMED.

---

## 3. Loss Categories and Definitions

### Availability Losses (Unplanned Downtime)

| Loss Code | Loss Description | Examples |
|---|---|---|
| **A01** | Equipment breakdown | Filler pump failure, capper jam, conveyor belt break |
| **A02** | Tooling / minor adjustment | Format parts not seated correctly; minor adjustments during run |
| **A03** | Material shortage | RM/PM not available at line start; bulk not ready |
| **A04** | Quality hold / inspection | Line stopped pending QA in-process check or hold decision |
| **A05** | Utility failure | Air pressure drop, steam loss, chilled water failure |
| **A06** | Other unplanned downtime | Operator absence, shift handover delays |

### Planned Stoppages (Tracked Separately)

| Loss Code | Loss Description | Examples |
|---|---|---|
| **P01** | Planned changeover (CIP + format change) | Product-to-product or size-to-size change |
| **P02** | Scheduled preventive maintenance | PM window per maintenance schedule |
| **P03** | Scheduled cleaning (non-changeover) | End-of-week tank cleaning, hygiene cleans |
| **P04** | Trials / NPD runs | New product trials, process optimisation runs |

### Performance Losses (Speed Loss)

| Loss Code | Loss Description | Examples |
|---|---|---|
| **S01** | Reduced speed – product quality | Running below rated speed to avoid defects (e.g., leaking caps) |
| **S02** | Minor stoppages / micro-stops | < 5 min stoppages not logged as breakdowns (jams, sensor faults) |
| **S03** | Operator-paced section | Manual operation pacing the line below rated speed |

### Quality Losses

| Loss Code | Loss Description | Examples |
|---|---|---|
| **Q01** | Start-up rejects | First-fill rejects while line reaching steady state |
| **Q02** | In-process defects (cosmetic) | Label skew, print quality, cap torque failures |
| **Q03** | In-process defects (functional) | Underfill, overfill, seal integrity failures |
| **Q04** | Rework | Product reworked due to label error, coding error |
| **Q05** | Scrap | Product destroyed (not reworkable) |

### Material (Yield) Losses

| Loss Code | Loss Description | Examples |
|---|---|---|
| **M01** | Bulk making yield loss | Residue left in vessel, evaporation losses |
| **M02** | Filling overfill | Product dispensed above nominal fill weight (give-away) |
| **M03** | Cleaning / flush losses | Product lost during CIP flush |
| **M04** | Trial and calibration losses | First-fills, calibration samples, stability samples |
| **M05** | Damage and breakage | Broken bottles, crushed tubes in packing |

---

## 4. OEE Data by Line

> **Note:** Populate the table below with actual OEE data from SAP, MES, or line logs. Update monthly.

### Current OEE by Line (Rolling 12-Month Average)

| Line | Availability % | Performance % | Quality % | **OEE %** | Target OEE % | Gap |
|---|---|---|---|---|---|---|
| Line 1 | *(to be filled)* | *(to be filled)* | *(to be filled)* | *(to be filled)* | 75% | — |
| Line 2 | *(to be filled)* | *(to be filled)* | *(to be filled)* | *(to be filled)* | 75% | — |
| Line 3 | *(to be filled)* | *(to be filled)* | *(to be filled)* | *(to be filled)* | 72% | — |
| Line 4 | *(to be filled)* | *(to be filled)* | *(to be filled)* | *(to be filled)* | 68% | — |
| Line 5 | *(to be filled)* | *(to be filled)* | *(to be filled)* | *(to be filled)* | 70% | — |

### OEE Trend (Monthly — Rolling 12 Months)

> Insert trend chart here (export from OEE dashboard or MES).

---

## 5. Top Losses Analysis (Pareto)

The Pareto analysis identifies the **vital few losses** that account for the majority of downtime and production loss. The top losses by downtime minutes (plant-wide) are reviewed monthly.

### Top 10 Losses — Pareto Template

| Rank | Loss Code | Loss Description | Line(s) | Monthly Minutes Lost | Cumulative % |
|---|---|---|---|---|---|
| 1 | P01 | Planned changeover (CIP + format) | All | *(to be filled)* | *(to be filled)* |
| 2 | A01 | Equipment breakdown – gear pump seal (Line 3) | Line 3 | *(to be filled)* | *(to be filled)* |
| 3 | S02 | Minor stoppages / micro-stops | All | *(to be filled)* | *(to be filled)* |
| 4 | A03 | Material shortage at line | All | *(to be filled)* | *(to be filled)* |
| 5 | P01 | Film roll changeover (Line 5) | Line 5 | *(to be filled)* | *(to be filled)* |
| 6 | S01 | Reduced speed – label accuracy (Line 1, 90 ml) | Line 1 | *(to be filled)* | *(to be filled)* |
| 7 | A01 | Equipment breakdown – tube seal failures (Line 4) | Line 4 | *(to be filled)* | *(to be filled)* |
| 8 | Q01 | Start-up rejects | All | *(to be filled)* | *(to be filled)* |
| 9 | A04 | Quality hold / in-process check delay | All | *(to be filled)* | *(to be filled)* |
| 10 | M02 | Bulk filling give-away (overfill) | Lines 1–3 | *(to be filled)* | *(to be filled)* |

> **Instructions:** Populate from monthly downtime reports. Track trend month-on-month.
> Top losses drive action plans — see [Action Plans](../08-action-plans/README.md).

---

## 6. Root Cause Analysis

For each top loss, a root cause analysis (RCA) is conducted using the **5-Why methodology** or **Fishbone (Ishikawa) diagram**.

### RCA Template

Each loss event or recurring loss pattern is documented using the following structure:

| Field | Content |
|---|---|
| **Loss ID** | Unique reference (e.g., RCA-2026-001) |
| **Loss Code** | From loss category list (e.g., A01) |
| **Date / Period** | When loss occurred |
| **Line** | Affected line(s) |
| **Description** | What happened |
| **Impact** | Minutes of downtime / units lost / cost |
| **5-Why Analysis** | Why 1 → Why 2 → Why 3 → Why 4 → Root Cause |
| **Corrective Action** | Immediate fix |
| **Preventive Action** | Systemic fix to prevent recurrence |
| **Owner** | Responsible person |
| **Due Date** | Target completion |
| **Status** | Open / In Progress / Closed |

### Example RCA — Line 3 Gear Pump Seal Failure

| Field | Content |
|---|---|
| **Loss ID** | RCA-2026-001 |
| **Loss Code** | A01 |
| **Date / Period** | Recurring — identified as top loss in Q1 2026 |
| **Line** | Line 3 |
| **Description** | Gear pump seal fails after approximately 4–6 weeks of operation, causing product leakage and line stoppage |
| **Impact** | ~90 min per event; ~2 events/month = 180 min/month unplanned downtime |
| **5-Why Analysis** | **Why 1:** Line stopped → pump leaking. **Why 2:** Pump seal worn → running beyond design life. **Why 3:** Seal not replaced on schedule → no PM trigger in CMMS. **Why 4:** Seal life data not loaded in CMMS → asset history not captured at installation. **Root Cause:** PM task for seal replacement not set up in CMMS at line commissioning. |
| **Corrective Action** | Replace all seals immediately; add PM task to CMMS. |
| **Preventive Action** | Set CMMS PM trigger at 3-week intervals; validate with equipment manufacturer's recommended interval. |
| **Owner** | Engineering Manager |
| **Due Date** | 2026-07-15 |
| **Status** | In Progress |

> **Note:** All RCA records are maintained in the CI tracking system / CMMS. Link action items to [Action Plans](../08-action-plans/README.md).
