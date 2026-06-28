# 08 – Action Plans

> **Last Reviewed:** 2026-06-28
> **Owner:** Plant Manager / Continuous Improvement Lead

---

## Contents

1. [Action Plan Overview](#1-action-plan-overview)
2. [Initiative Register](#2-initiative-register)
3. [Touchless Planning Initiatives](#3-touchless-planning-initiatives)
4. [OEE / Loss Reduction Initiatives](#4-oee--loss-reduction-initiatives)
5. [Material Loss Reduction Initiatives](#5-material-loss-reduction-initiatives)
6. [Governance and Review Cadence](#6-governance-and-review-cadence)

---

## 1. Action Plan Overview

This section documents all improvement initiatives for the BKK Hair Care plant. Initiatives are derived from:
- **Value stream mapping** kaizen opportunities (see [VSM](../07-value-stream-mapping/README.md))
- **Operational losses** root cause analysis (see [Operational Losses](../06-operational-losses/README.md))
- **Planning process** pain points (see [Planning Processes](../04-planning-processes/README.md#7-current-planning-pain-points))
- **Constraint** mitigation plans (see [Constraints](../05-constraints/README.md#7-constraint-register))

### Initiative Priority Framework

Initiatives are prioritised using a simple **Impact × Ease** matrix:

| Priority | Criteria |
|---|---|
| 🔴 **P1 – Critical** | High impact on safety, quality, or volume; must be resolved immediately |
| 🟠 **P2 – High** | Significant loss reduction or capacity gain; targeted within 3 months |
| 🟡 **P3 – Medium** | Moderate improvement; targeted within 6 months |
| 🟢 **P4 – Low** | Incremental gain; targeted within 12 months |

---

## 2. Initiative Register

| ID | Initiative Name | Category | Priority | Owner | Target Date | Status | Linked Losses / Constraints |
|---|---|---|---|---|---|---|---|
| **AP-001** | SMED on Line 1 (90 ml ↔ 340 ml changeover) | OEE / Changeover | 🟠 P2 | Production Manager | Q3 2026 | 🔵 In Progress | C-001, KZ-02 |
| **AP-002** | Gear pump seal PM schedule (Line 3) | OEE / Maintenance | 🔴 P1 | Engineering Manager | Q3 2026 | 🔵 In Progress | C-002, RCA-2026-001 |
| **AP-003** | Auto-cartoner on Line 4 (capex) | Capacity / OEE | 🟡 P3 | Engineering Manager | Q1 2027 | 🟡 Planned | C-003, KZ-04 |
| **AP-004** | Fragrance dual-source qualification | Supply Risk | 🟠 P2 | Procurement Manager | Q3 2026 | 🔵 In Progress | C-004 |
| **AP-005** | Rapid microbiological testing method validation | Quality / Lead Time | 🟡 P3 | QA Manager | Q2 2027 | 🟡 Planned | KZ-01 |
| **AP-006** | APS implementation (touchless scheduling) | Planning / TP-01 | 🟠 P2 | SC Manager | *(TBD)* | 🔴 Not Started | TP-01, KZ-07 |
| **AP-007** | MES / real-time OEE data integration | Planning / TP-02 | 🟠 P2 | Engineering / IT | *(TBD)* | 🔴 Not Started | TP-02, KZ-05 |
| **AP-008** | SMED on Line 5 (film roll changeover) | OEE / Changeover | 🟡 P3 | Production Manager | Q4 2026 | 🟡 Planned | KZ-06 |
| **AP-009** | Bulk-to-filling schedule synchronisation | Planning / TP-06 | 🟠 P2 | Plant Planner | Q3 2026 | 🔵 In Progress | TP-06, KZ-03 |
| **AP-010** | Compressed air system upgrade (capex) | Utility / Infrastructure | 🟡 P3 | Engineering Manager | Q2 2027 | 🟡 Planned | C-008 |
| **AP-011** | Dynamic safety stock modelling (IBP) | Planning / TP-04 | 🟡 P3 | Demand Planner | *(TBD)* | 🔴 Not Started | TP-04 |
| **AP-012** | Planning cross-training programme | People | 🟡 P3 | SC Manager | Q3 2026 | 🔵 In Progress | C-007 |
| **AP-013** | Filling overfill reduction (give-away) | Material Loss | 🟠 P2 | Production Manager / QA | Q3 2026 | 🔵 In Progress | M02 |
| **AP-014** | Digital planning cockpit / control tower | Planning / TP-07 | 🟢 P4 | SC Manager / IT | *(TBD)* | 🔴 Not Started | TP-07 |

> **Status key:** 🔴 Not Started | 🟡 Planned | 🔵 In Progress | ✅ Complete | ⏸ On Hold

---

## 3. Touchless Planning Initiatives

### AP-006 — APS Implementation (Touchless Scheduling)

| Attribute | Details |
|---|---|
| **Objective** | Implement an Advanced Planning & Scheduling (APS) tool to automate production scheduling, eliminating manual Excel scheduling and enabling sequence optimisation |
| **Current State** | 2–4 hrs/day manual scheduling; no automated changeover optimisation; Excel-based |
| **Target State** | APS generates optimised daily/weekly line schedule in < 30 min; planner reviews and approves exceptions only |
| **Key Activities** | 1. Define scheduling requirements and tool selection criteria. 2. Evaluate APS tools (SAP PP/DS, Preactor, Quintiq, etc.). 3. Pilot on Lines 1–2. 4. Full rollout. 5. Integration with SAP PP and MES. |
| **Success Metrics** | Planning time < 30 min/day; Schedule adherence ≥ 97%; Changeover minutes reduced by ≥ 20% |
| **Dependencies** | MES data feed (AP-007); Clean master data in SAP (run rates, changeover matrix) |
| **Risks** | Master data quality; change management (planner adoption) |

### AP-007 — MES / Real-Time OEE Data Integration

| Attribute | Details |
|---|---|
| **Objective** | Implement a Manufacturing Execution System (MES) or digital OEE tool to capture real-time line performance data, replacing paper logbooks |
| **Current State** | Paper-based logbooks; data manually entered into SAP with 24-hr lag; OEE not available in real time |
| **Target State** | Real-time OEE dashboard visible to shift managers and planners; automated downtime categorisation; integration with SAP PP |
| **Key Activities** | 1. Define MES requirements. 2. Select tool (SAP ME, Tulip, Ignition SCADA, etc.). 3. Pilot on Line 1. 4. Roll out to all lines. 5. Integrate with SAP PP and APS. |
| **Success Metrics** | OEE data available within 5 min of event; downtime root-cause capture rate ≥ 95%; planning team uses live data for same-day schedule adjustments |
| **Dependencies** | Network infrastructure on production floor; IT project resourcing |
| **Risks** | Network connectivity; operator adoption; data governance |

### AP-009 — Bulk-to-Filling Schedule Synchronisation

| Attribute | Details |
|---|---|
| **Objective** | Synchronise the bulk making plan with the filling schedule to eliminate bulk holding time and material shortage stoppages at filling lines |
| **Current State** | Bulk plan and filling plan managed separately; bulk shortages at filling cause stoppages; excess bulk held in tanks |
| **Target State** | Bulk making triggered by filling consumption signals; bulk tank inventory reduced to < 4 hours coverage |
| **Key Activities** | 1. Map current bulk-to-filling handshake process. 2. Define kanban trigger rules for bulk making. 3. Implement in SAP or via visual kanban board. 4. Train mixing and filling teams on pull system. |
| **Success Metrics** | Bulk shortage stoppages at filling reduced to zero; bulk holding inventory < 4 hrs coverage; bulk make schedule adherence ≥ 98% |
| **Dependencies** | Accurate bulk consumption rates in SAP; Mixer capacity analysis |
| **Risks** | Inaccurate cycle times; mixer capacity insufficient to support pull system during peak demand |

---

## 4. OEE / Loss Reduction Initiatives

### AP-001 — SMED on Line 1 (90 ml ↔ 340 ml Changeover)

| Attribute | Details |
|---|---|
| **Objective** | Reduce changeover time on Line 1 between 90 ml and 340 ml formats from 3–4 hrs to ≤ 2 hrs using SMED methodology |
| **Current State** | 3–4 hr changeover; all activities performed sequentially with line stopped |
| **Target State** | ≤ 2 hr changeover; internal and external activities separated; format part pre-staging completed before line stop |
| **Key Activities** | 1. Film and time all changeover activities (video study). 2. Classify internal vs. external activities. 3. Convert internal to external activities (pre-stage format parts, pre-clean components off-line). 4. Standardise and document new method (SOP). 5. Train operators. 6. Measure and verify. |
| **Success Metrics** | Changeover time ≤ 2 hrs; ≥ 20 min additional uptime per changeover event |
| **Target Date** | Q3 2026 |
| **Owner** | Production Manager |

### AP-002 — Gear Pump Seal PM Schedule (Line 3)

| Attribute | Details |
|---|---|
| **Objective** | Eliminate unplanned gear pump seal failures on Line 3 by implementing a preventive maintenance schedule |
| **Current State** | Seals fail every 4–6 weeks; ~90 min downtime per event; ~2 events/month |
| **Target State** | Zero unplanned seal failures; planned seal replacement every 3 weeks |
| **Key Activities** | 1. Replace all current seals immediately. 2. Create CMMS PM task with 3-week interval. 3. Stock replacement seals (min 4 sets on-hand at all times). 4. Validate optimal interval with equipment manufacturer. 5. Review after 3 months. |
| **Success Metrics** | Zero unplanned pump seal failures within 3 months of implementation |
| **Target Date** | Q3 2026 |
| **Owner** | Engineering Manager |

### AP-008 — SMED on Line 5 (Film Roll Changeover)

| Attribute | Details |
|---|---|
| **Objective** | Reduce film roll changeover time on Line 5 from ~25 min to ≤ 10 min |
| **Current State** | ~25 min per roll change; up to 8 changeovers/shift = up to 200 min/shift downtime |
| **Target State** | ≤ 10 min per roll change; pre-loaded roll staging; automated roll splicer (if applicable) |
| **Key Activities** | 1. Time current film roll changeover. 2. Assess feasibility of automatic film splicer. 3. Implement pre-staging (external activities) in parallel with production. 4. Update SOP and train operators. |
| **Success Metrics** | Film roll changeover ≤ 10 min; ≥ 120 min/shift additional running time |
| **Target Date** | Q4 2026 |
| **Owner** | Production Manager |

---

## 5. Material Loss Reduction Initiatives

### AP-013 — Filling Overfill Reduction (Give-Away)

| Attribute | Details |
|---|---|
| **Objective** | Reduce filling give-away on Lines 1–3 (overfill above nominal fill weight) to reduce material cost and improve yield |
| **Current State** | Average overfill estimated at 1–2% above nominal fill weight; annual cost impact to be quantified |
| **Target State** | Average overfill < 0.5% above nominal fill weight |
| **Key Activities** | 1. Audit current fill weight data (average, standard deviation) per line per SKU. 2. Identify root causes of fill weight variation (filler calibration, product viscosity variation, run speed). 3. Implement statistical process control (SPC) for fill weight monitoring. 4. Recalibrate fillers; tighten fill weight control limits. 5. Train operators on SPC use. |
| **Success Metrics** | Average overfill ≤ 0.5% above nominal; fill weight Cpk ≥ 1.33 |
| **Target Date** | Q3 2026 |
| **Owner** | Production Manager / QA Manager |

---

## 6. Governance and Review Cadence

| Review | Frequency | Participants | Focus |
|---|---|---|---|
| **Daily CI Standup** | Daily (15 min) | Shift Manager, CI Lead | Yesterday's losses; in-day actions |
| **Weekly OEE Review** | Weekly | Production Mgr, Engineering Mgr, CI Lead | OEE trends; top losses; RCA progress |
| **Monthly S&OP Pre-Review** | Monthly | Plant Mgr, SC Mgr, Prod Mgr, QA Mgr | Action plan progress; constraint register update |
| **Quarterly VSM Review** | Quarterly | Plant Mgr + all function heads | Progress vs. future state VSM; kaizen prioritisation |
| **Annual CI Planning** | Annually | Plant Mgr + all function heads | Define next year's initiative portfolio; capex requests |

> **Action plan dashboard:** A consolidated action plan status is maintained and reviewed at each Weekly OEE Review and Monthly S&OP Pre-Review. Owners are accountable for updating their initiative status at least weekly.
