# 04 – Planning Processes

> **Last Reviewed:** 2026-06-28
> **Owner:** Supply Chain / Planning Manager

---

## Contents

1. [Planning Hierarchy Overview](#1-planning-hierarchy-overview)
2. [Demand Planning](#2-demand-planning)
3. [Supply and Capacity Planning (S&OP / IBP)](#3-supply-and-capacity-planning-sop--ibp)
4. [Master Production Scheduling (MPS)](#4-master-production-scheduling-mps)
5. [Materials Requirements Planning (MRP)](#5-materials-requirements-planning-mrp)
6. [Detailed Production Scheduling](#6-detailed-production-scheduling)
7. [Current Planning Pain Points](#7-current-planning-pain-points)
8. [Touchless Planning Roadmap](#8-touchless-planning-roadmap)

---

## 1. Planning Hierarchy Overview

BKK's planning operates across four time horizons:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  HORIZON          PROCESS               TOOL          CADENCE     HORIZON   │
│─────────────────────────────────────────────────────────────────────────────│
│  Long Range    Strategic Capacity Plan   IBP / Excel   Quarterly   18+ months│
│  Mid Range     S&OP / Rough-Cut Cap.     IBP           Monthly     3–18 months│
│  Short Range   Master Production Sched.  SAP PP / APS  Weekly      0–13 weeks│
│  Execution     Detailed Line Schedule    SAP PP / Excel Daily       0–2 weeks │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Demand Planning

| Attribute | Details |
|---|---|
| **Process** | Statistical baseline forecast + commercial team overrides |
| **Tool** | SAP IBP for Demand (or equivalent) |
| **Cadence** | Monthly consensus cycle |
| **Horizon** | 18 months rolling |
| **Output** | Unconstrained demand plan (by SKU, by month) |
| **Owner** | Demand Planner / Commercial Finance |

### Key Inputs
- Historical sales data (POS / shipment actuals)
- Promotional calendar and new product launch pipeline
- Customer / market intelligence
- Seasonality indices (see [Production Volumes – Seasonality](../03-production-volumes/README.md#5-volume-trends-and-seasonality))

### Key Outputs
- Approved demand plan (consensus forecast) uploaded to IBP
- Volume risk and opportunity register

---

## 3. Supply and Capacity Planning (S&OP / IBP)

| Attribute | Details |
|---|---|
| **Process** | Integrated Business Planning (IBP) / S&OP |
| **Tool** | SAP IBP for Supply + Response |
| **Cadence** | Monthly S&OP cycle (pre-S&OP → S&OP meeting) |
| **Horizon** | 3–18 months rolling |
| **Output** | Constrained production plan, capacity utilisation by line |
| **Owner** | Supply Chain Manager / Plant Planning Manager |

### S&OP Monthly Cycle

| Week | Activity | Participants |
|---|---|---|
| Week 1 | Demand review — finalise consensus forecast | Demand Planner, Commercial |
| Week 2 | Supply review — check capacity, identify gaps | Supply Planner, Plant Planner |
| Week 3 | Pre-S&OP — resolve gaps, prepare scenarios | Supply Chain Lead, Finance |
| Week 4 | Executive S&OP — approve plan | Plant Manager, SC Manager, Finance Director |

### Rough-Cut Capacity Planning (RCCP)

RCCP validates the production plan against available line capacity before it is accepted into the MPS:
1. Convert plan volumes (cases) to line hours using standard run rates.
2. Compare required hours vs. available hours (net of planned downtime).
3. Identify over-/under-loaded lines and resolve by levelling, outsourcing, or demand shaping.

---

## 4. Master Production Scheduling (MPS)

| Attribute | Details |
|---|---|
| **Process** | Frozen-horizon scheduling with weekly review |
| **Tool** | SAP PP (MPS run) / APS (if applicable) |
| **Cadence** | Weekly MPS review meeting |
| **Frozen Horizon** | 2 weeks (no changes without Plant Manager approval) |
| **Firm Horizon** | 4 weeks (changes require planning approval) |
| **Output** | Planned production orders by week and line |
| **Owner** | Plant Production Planner |

### MPS Inputs
- Approved constrained supply plan (from S&OP/IBP)
- Current inventory levels (FG, WIP, bulk)
- Safety stock targets
- Material availability confirmation (from MRP)
- Confirmed plant capacity (downtime schedule, maintenance windows)

### MPS Review Meeting Agenda (Weekly)

1. Review previous week's performance vs. MPS.
2. Review material coverage for next 4 weeks.
3. Confirm or adjust the 2-week frozen schedule.
4. Raise any capacity or material risks to the supply chain manager.

---

## 5. Materials Requirements Planning (MRP)

| Attribute | Details |
|---|---|
| **Process** | Net requirements calculation → purchase / production requisitions |
| **Tool** | SAP PP/MM (MRP run) |
| **Cadence** | Daily MRP run (or on-demand) |
| **Output** | Purchase requisitions (RM/PM), planned orders (bulk / semi-finished) |
| **Owner** | Material Planner / Procurement |

### MRP Parameters (Key Settings per Material)

| Parameter | Description | Typical Setting |
|---|---|---|
| **MRP Type** | Planning strategy (MRP, reorder point, etc.) | PD (MRP) for most materials |
| **Lot Size** | Minimum order quantity, rounding values | Per supplier agreement |
| **Safety Stock** | Buffer to absorb demand/supply variability | Based on lead time × demand variability |
| **Lead Time** | Planned delivery lead time from supplier | 2–12 weeks depending on material |
| **Procurement Type** | External (E) or in-house production (F) | E for RM/PM; F for bulk |

> **Note:** MRP master data quality is critical for planning accuracy. Outdated lead times or incorrect lot sizes are a common root cause of planning exceptions. Regular MRP parameter reviews are included in the planning audit cycle.

---

## 6. Detailed Production Scheduling

| Attribute | Details |
|---|---|
| **Process** | Sequence planned orders into a shift-by-shift line schedule |
| **Tool** | SAP PP scheduling board / Excel-based line schedule |
| **Cadence** | Daily scheduling meeting (shift handover) |
| **Output** | Daily/shift-level line schedule distributed to production |
| **Owner** | Shift Manager / Production Planner |

### Scheduling Principles

1. **Sequence to minimise changeover:** Group similar products (formula family, viscosity) to reduce CIP time.
2. **Respect frozen horizon:** Do not move production orders within the 2-week frozen horizon without approval.
3. **Material confirmation:** Confirm RM/PM availability before confirming the schedule.
4. **Maintenance windows:** Reserve scheduled maintenance slots (no production booking during PM windows).
5. **Quality hold / rework:** Factor in rework orders where applicable; coordinate with QA for release timelines.

---

## 7. Current Planning Pain Points

The following pain points have been identified through the value stream mapping exercise and team workshops:

| # | Pain Point | Impact | Root Cause |
|---|---|---|---|
| 1 | **High manual effort in scheduling** | 2–4 hours/day spent on Excel-based schedule updates | No APS tool; manual translation from SAP planned orders |
| 2 | **Frequent last-minute schedule changes** | Reactive behaviour, disrupts line efficiency | Late demand changes, material shortages, equipment breakdowns |
| 3 | **MRP exception messages not actioned** | Shortages or excess inventory built up | High volume of exceptions; no triage process |
| 4 | **Lack of real-time visibility on line performance** | Schedule deviations discovered late | No MES or live OEE dashboard integrated with planning |
| 5 | **Safety stock targets not regularly reviewed** | Over- or under-stocking | Annual review only; no dynamic safety stock model |
| 6 | **Changeover time not systematically tracked** | Cannot optimise scheduling sequences | Data captured in paper logbooks, not in SAP |
| 7 | **Bulk make plan not integrated with filling schedule** | Bulk shortages cause filling stoppages | Separate bulk and filling plans not synchronised |

---

## 8. Touchless Planning Roadmap

**Definition:** Touchless planning refers to a state where the end-to-end planning process (demand sensing → supply planning → scheduling → execution) runs with minimal manual intervention, driven by system automation, real-time data, and pre-defined decision rules.

### Maturity Model

| Level | Description | Current State | Target State |
|---|---|---|---|
| **Level 1** | Manual | All planning done manually in spreadsheets | *(baseline)* | |
| **Level 2** | System-assisted | SAP/IBP used; manual overrides frequent | **BKK current** | |
| **Level 3** | System-driven | Plans auto-generated; exceptions managed by planners | | **Year 1 target** |
| **Level 4** | Largely automated | Automated execution within guardrails; planner focuses on exceptions | | Year 2–3 target |
| **Level 5** | Fully touchless | AI-driven demand sensing + autonomous scheduling + self-correcting execution | | Long-term vision |

### Touchless Planning Initiative Workstreams

| Workstream | Description | Owner | Target Completion |
|---|---|---|---|
| **TP-01** | APS (Advanced Planning & Scheduling) implementation | SC Manager | *(to be defined)* |
| **TP-02** | MES / real-time OEE data integration | Engineering / IT | *(to be defined)* |
| **TP-03** | Automated MRP exception triage and resolution | Material Planner | *(to be defined)* |
| **TP-04** | Dynamic safety stock modelling (IBP integration) | Demand Planner | *(to be defined)* |
| **TP-05** | Changeover optimisation algorithm (sequence planning) | Plant Planner | *(to be defined)* |
| **TP-06** | Bulk-to-filling schedule synchronisation | Production Planner | *(to be defined)* |
| **TP-07** | Digital planning cockpit / control tower | SC Manager / IT | *(to be defined)* |

> See [Action Plans](../08-action-plans/README.md) for detailed initiative plans, milestones, and owners.
