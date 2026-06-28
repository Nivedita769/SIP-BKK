# 07 – Value Stream Mapping

> **Last Reviewed:** 2026-06-28
> **Owner:** Continuous Improvement Lead / Plant Manager

---

## Contents

1. [VSM Overview and Purpose](#1-vsm-overview-and-purpose)
2. [VSM Scope and Boundaries](#2-vsm-scope-and-boundaries)
3. [Current State Value Stream Map](#3-current-state-value-stream-map)
4. [Current State Key Metrics](#4-current-state-key-metrics)
5. [Waste Identification (Current State)](#5-waste-identification-current-state)
6. [Future State Value Stream Map](#6-future-state-value-stream-map)
7. [Gap Analysis: Current vs. Future State](#7-gap-analysis-current-vs-future-state)
8. [VSM Workshop Log](#8-vsm-workshop-log)

---

## 1. VSM Overview and Purpose

**Value Stream Mapping (VSM)** is a lean manufacturing technique used to visualise, analyse, and improve the flow of materials and information required to bring a product from raw material to finished goods delivery.

### Purpose at BKK

The VSM at BKK serves two primary objectives:
1. **Identify operational losses** — map every step in the value stream to surface waste (non-value-adding activities), including waiting, overproduction, motion, transport, over-processing, inventory, and defects.
2. **Define the path to touchless planning** — use the future-state map to design a planning and execution model that minimises manual intervention and maximises flow.

### VSM Methodology Used

BKK uses the standard **Lean VSM methodology** (Rother & Shook, *Learning to See*):
- Draw the **current state** map to reflect how the plant actually operates today.
- Identify waste and improvement opportunities using the 8 wastes of lean (TIMWOODS).
- Design the **future state** map to show the target operating model.
- Define **kaizen bursts** (improvement projects) to close the gap.

---

## 2. VSM Scope and Boundaries

| Attribute | Details |
|---|---|
| **Product Family** | High-volume shampoo (standard and moisturising range — 170 ml and 340 ml bottles) |
| **Start Boundary** | Receipt of raw materials and packaging materials at BKK warehouse |
| **End Boundary** | Finished goods despatched to regional distribution centre |
| **Excluded** | Supplier operations upstream; distribution centre operations downstream |
| **VSM Participants** | Plant Manager, Production Manager, Planning Manager, QA Manager, Engineering Manager, CI Lead, Shift Managers |
| **VSM Date** | *(to be filled)* |

> **Note:** The initial VSM focuses on the high-volume shampoo product family on Lines 1 and 2, as these represent the highest volume and highest loss opportunity. Subsequent VSMs will cover conditioners, treatments, and sachets.

---

## 3. Current State Value Stream Map

```
CUSTOMER / DISTRIBUTION CENTRE
   ▲
   │ Finished Goods Delivery
   │ (OTIF target ≥ 98%)
   │
┌──┴──────────────────────────────────────────────────────────────────────┐
│                     PLANT INFORMATION FLOW                              │
│                                                                         │
│  IBP / S&OP     →   MPS (SAP PP)   →   Daily Schedule (Excel)          │
│  (Monthly)          (Weekly)            (Shift-level, manual)           │
│                                              │                          │
│                                              ▼                          │
└─────────────────────────────────────────────────────────────────────────┘
         │                                     │
         │ Purchase Orders                     │ Production Orders
         ▼                                     ▼
┌────────────────┐                   ┌─────────────────────┐
│   SUPPLIER     │                   │  PRODUCTION PLANNING │
│  (RM / PM)     │                   │  (MPS + MRP)         │
└───────┬────────┘                   └──────────┬──────────┘
        │ RM/PM delivery (2–12 wk LT)           │
        ▼                                       │
┌────────────────┐     PUSH                     │
│  RM/PM         │ ──────────────────────────── │
│  Warehouse     │                              │
│  (Receipt +    │     ┌────────────────┐       │
│   QC sampling) │────▶│  Bulk Making   │◀──────┘
└────────────────┘     │  (Weighing +   │
                        │  Mixing)       │
                        │  CT: 3–4 hrs   │
                        │  Batch: 1–10 t │
                        └───────┬────────┘
                                │ PUSH (bulk tank)
                                ▼
                        ┌───────────────┐
                        │  Bulk Holding  │
                        │  (Intermediate │
                        │   Tank)        │
                        │  Inventory:    │
                        │  0.5–2 days    │
                        └───────┬───────┘
                                │
                                ▼
┌──────────────────────────────────────────────────────┐
│                  FILLING / PACKING LINES              │
│                                                      │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐     │
│  │  Fill &    │  │  Cap &     │  │  Label &   │     │
│  │  Check     │  │  Seal      │  │  Code      │     │
│  │ CT: 0.6s   │  │ CT: 0.6s   │  │ CT: 0.6s   │     │
│  │/unit       │  │/unit       │  │/unit       │     │
│  └────────────┘  └────────────┘  └────────────┘     │
│           │                               │          │
│           └───────────────────────────────┘          │
│                          │                           │
│               ┌──────────▼──────────┐                │
│               │  End-of-Line Packing │                │
│               │  (Tray / Shrink /   │                │
│               │  Palletise)         │                │
│               └──────────┬──────────┘                │
└──────────────────────────┼───────────────────────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │  QC Release     │
                  │  (Hold 1–3 days)│
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │  FG Warehouse   │
                  │  (Storage:      │
                  │  3–7 days avg)  │
                  └────────┬────────┘
                           │
                           ▼
              DISTRIBUTION CENTRE (CUSTOMER)
```

> **Note:** A full-detail VSM drawing (with data boxes for each process step, inventory triangles, push/pull arrows, and timeline) is maintained as a separate diagram file. The text representation above provides structural orientation. Attach the visual VSM file here when completed.

---

## 4. Current State Key Metrics

### Process Step Data (Current State)

| Process Step | Cycle Time (CT) | Process Time | Changeover Time | Uptime / Availability | Yield |
|---|---|---|---|---|---|
| RM/PM Receipt & QC Sampling | 1–2 days (QC hold) | Per shipment | N/A | N/A | 99%+ |
| Bulk Making (Weighing + Mixing) | 3–4 hrs/batch | 3–4 hrs | 1–2 hrs (clean) | ~85% | ~99.5% |
| Bulk Transfer to Filling | 0.5–1 hr | 0.5–1 hr | N/A | ~95% | ~99.8% |
| Filling / Capping / Labelling (Line 1/2) | 0.6 s/unit | Continuous | 2–5 hrs | ~75% availability | ~98.5% |
| End-of-Line Packing | Matched to filling | Continuous | 30–60 min | ~80% | ~99% |
| QC Release Hold | 1–3 days | Lab test time | N/A | N/A | ~99% RFT |
| FG Storage | 3–7 days avg | N/A | N/A | N/A | N/A |

### Lead Time Calculation (Current State)

| Step | Value-Adding Time | Non-Value-Adding Time (Wait/Hold) |
|---|---|---|
| RM/PM in warehouse (pre-use) | — | 1–5 days inventory |
| Bulk making | 3–4 hrs | 0–4 hrs (bulk wait in tank) |
| Filling/packing | 2–6 hrs per batch | 1–2 hrs (changeover, QA hold) |
| QC release | Lab testing (2–4 hrs) | 1–3 days hold |
| FG storage | — | 3–7 days inventory |
| **Total end-to-end lead time** | **~6–12 hrs value-add** | **~5–16 days non-value-add** |

> **Observation:** Value-adding time is a small fraction of the total lead time. The majority of lead time is inventory (wait time), which is driven by batch sizes, planning frequency, and QC release holds.

---

## 5. Waste Identification (Current State)

Using the **8 Wastes of Lean (TIMWOODS)**:

| Waste | Observed at BKK | Examples | Priority |
|---|---|---|---|
| **T – Transport** | Moderate | Bulk transferred from mixing to filling via pump; FG moved to/from warehouse | Low |
| **I – Inventory** | High | RM/PM safety stock, bulk holding tanks, FG warehouse | High |
| **M – Motion** | Moderate | Manual cartoning on Line 4; paper logbook entries | Medium |
| **W – Waiting** | High | QC release hold 1–3 days; bulk waiting in tank; line waiting for materials | High |
| **O – Overproduction** | Medium | Producing against MPS even when demand signal changes | Medium |
| **O – Over-processing** | Low | Multiple manual re-entries of production data (logbook → SAP) | Medium |
| **D – Defects** | Medium | Seal failures on Line 4; label skew on Line 1; tube seal rejects | Medium |
| **S – Skills (unused talent)** | Medium | Operators not empowered to resolve minor stoppages; planning key-person dependency | Medium |

### Kaizen Opportunities Identified in Current State

| # | Opportunity | Waste Type | Potential Impact |
|---|---|---|---|
| KZ-01 | Reduce QC release hold time through rapid micro testing | Waiting | −1 to 2 days lead time |
| KZ-02 | Implement SMED on Line 1 (90 ml ↔ 340 ml changeover) | Waiting | −1 to 2 hrs per changeover |
| KZ-03 | Automate bulk-to-filling transfer scheduling (synchronise bulk plan with filling plan) | Inventory, Waiting | Reduce bulk holding time |
| KZ-04 | Install auto-cartoner on Line 4 (eliminate manual cartoning bottleneck) | Motion, Waiting | +40% throughput on Line 4 |
| KZ-05 | Implement real-time OEE data capture (MES / digital andon) | Over-processing | Faster response to losses |
| KZ-06 | SMED on Line 5 film roll changeover | Waiting | −15 min per roll change |
| KZ-07 | APS implementation for automated scheduling | Over-processing, Waiting | Remove 2–4 hrs/day manual scheduling |

---

## 6. Future State Value Stream Map

The future state map represents the **target operating model** after implementing the kaizen opportunities identified above. Key design principles for the future state:

### Future State Design Principles

1. **Pull, not push:** Trigger bulk making and filling based on actual consumption signals (kanban or APS-driven signals), not MPS push.
2. **Continuous flow:** Minimise buffers between process steps; synchronise bulk making to filling.
3. **Level scheduling:** Smooth the production schedule to reduce peaks and changeover frequency.
4. **Integrated information flow:** Replace manual Excel scheduling with APS-driven line schedule, integrated with SAP.
5. **Real-time visibility:** MES / digital andon provides live OEE and production attainment data to shift managers and planners.
6. **Rapid QC release:** Rapid micro testing reduces QC hold from 1–3 days to same-day or next-day release.

### Future State — Key Changes vs. Current State

| Process Area | Current State | Future State |
|---|---|---|
| **Scheduling** | Manual Excel, 2–4 hrs/day | APS-driven, automated sequence optimisation |
| **Bulk making → filling** | Push (batch plan) | Pull signal from filling (when tank drops below threshold) |
| **QC release** | 1–3 day hold | Same-day / next-day with rapid micro testing |
| **OEE tracking** | Paper logbook, manual SAP entry | Real-time MES / digital andon |
| **Changeover (Line 1)** | 3–4 hrs (90 ml ↔ 340 ml) | ≤ 2 hrs after SMED |
| **Line 4 cartoning** | Manual (bottleneck) | Automated cartoner |
| **FG lead time** | 5–16 days | Target: 3–8 days |

> **Note:** Future state VSM diagram is to be drawn during the VSM workshop. Attach completed drawing here.

---

## 7. Gap Analysis: Current vs. Future State

| Metric | Current State | Future State Target | Gap | Enabling Initiative |
|---|---|---|---|---|
| End-to-end lead time | 5–16 days | 3–8 days | −2–8 days | KZ-01, KZ-03, KZ-07 |
| OEE (average, all lines) | ~72% | ≥ 78% | +6 pp | KZ-02, KZ-04, KZ-05, KZ-06 |
| Changeover time (Line 1) | 3–4 hrs | ≤ 2 hrs | −1–2 hrs | KZ-02 (SMED) |
| Planning manual effort | 2–4 hrs/day | < 30 min/day | −1.5–3.5 hrs | KZ-07 (APS) |
| QC release time | 1–3 days | Same-day or next-day | −1–2 days | KZ-01 |

---

## 8. VSM Workshop Log

| Workshop # | Date | Participants | Output | Actions Raised |
|---|---|---|---|---|
| VSM-01 | *(to be scheduled)* | Plant Mgr, Prod Mgr, Planning Mgr, QA Mgr, Eng Mgr, CI Lead | Current state map | *(to be captured)* |
| VSM-02 | *(to be scheduled)* | Same + Finance | Future state map + kaizen plan | *(to be captured)* |
| VSM-03 (Review) | *(quarterly)* | All | Progress review vs. kaizen plan | *(to be captured)* |
