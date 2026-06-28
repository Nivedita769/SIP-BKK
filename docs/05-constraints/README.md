# 05 – Constraints

> **Last Reviewed:** 2026-06-28
> **Owner:** Production Manager / Plant Planning Manager

---

## Contents

1. [Constraint Categories](#1-constraint-categories)
2. [Capacity Constraints](#2-capacity-constraints)
3. [Material Constraints](#3-material-constraints)
4. [Quality and Regulatory Constraints](#4-quality-and-regulatory-constraints)
5. [People Constraints](#5-people-constraints)
6. [Utility and Infrastructure Constraints](#6-utility-and-infrastructure-constraints)
7. [Constraint Register](#7-constraint-register)

---

## 1. Constraint Categories

A **constraint** is any factor that limits the plant's ability to produce at full potential or meet the production plan. Constraints are classified into the following categories:

| Category | Description |
|---|---|
| **Capacity** | Equipment, line speed, or throughput limitations |
| **Material** | Raw material or packaging material availability, lead times, or quality |
| **Quality / Regulatory** | Formulation restrictions, labelling compliance, GMP requirements |
| **People** | Skill gaps, headcount, shift coverage, knowledge dependencies |
| **Utility / Infrastructure** | Utilities (steam, water, compressed air), warehouse space, cold chain |
| **Planning / Process** | Planning system limitations, data quality, schedule adherence |

---

## 2. Capacity Constraints

### Line-Level Capacity Constraints

| Line | Constraint | Impact | Details |
|---|---|---|---|
| **Line 1** | Labeller speed on 90 ml format | Limits line rate to ~3,600 units/hr on 90 ml (vs. 6,000 rated) | Label application accuracy degrades above 3,600 units/hr for small format |
| **Line 1** | 90 ml ↔ 340 ml tooling changeover | 3–4 hrs downtime per changeover | Large format-part set change required |
| **Line 2** | Viscosity-driven CIP requirement | Full CIP (3–5 hrs) when switching shampoo ↔ conditioner | Chemical compatibility requires complete clean |
| **Line 3** | Gear pump seal degradation | Unplanned stoppages 1–2×/week; avg. 1.5 hrs downtime per event | Pump seal life ~4–6 weeks at current run volumes |
| **Line 4** | Manual cartoning bottleneck | Limits throughput to 2,400 units/hr even if filler can run faster | Insufficient staffing for manual cartoning at higher speeds |
| **Line 5** | Film roll changeover | ~25 min per roll change, up to 8 changeovers/shift | High sachet volume requires frequent roll changes |

### Bulk Making (Mixing) Constraints

| Constraint | Impact | Details |
|---|---|---|
| **Mixer capacity (vessel size)** | Maximum batch size limited | Vessel capacity constrains batch size; multiple batches required for high-volume products |
| **Heating/cooling cycle time** | Long cycle for high-viscosity products | Conditioners and masks require controlled heat-cool cycles of 3–4 hrs/batch |
| **Cleaning between incompatible formulas** | Reduces available mixing time | Colour-care and standard formulas require full vessel clean to avoid cross-contamination |
| **Bulk transfer pumps** | Viscous products slow to transfer | High-viscosity bulk transfers take 30–60 min per batch to filling vessels |

---

## 3. Material Constraints

### Raw Material (RM) Constraints

| Material Type | Constraint | Impact | Mitigation |
|---|---|---|---|
| **Key actives** (e.g., conditioning agents, anti-dandruff actives) | Long lead times (8–12 weeks) from speciality suppliers | Risk of stockouts if demand spikes or supplier delays | Safety stock; dual-sourcing evaluation |
| **Fragrance compounds** | Custom-made; single-source | Supply vulnerability; long re-order lead time | 12-week minimum safety stock maintained |
| **Colour pigments** (for colour-care range) | Batch-to-batch colour variation | QC rejections; formula rework | Approved colour master standards; in-process colour check |

### Packaging Material (PM) Constraints

| Material Type | Constraint | Impact | Mitigation |
|---|---|---|---|
| **Printed bottles (pre-labelled)** | SKU proliferation → high MOQ from moulders | Excess inventory on slow-moving SKUs | Portfolio rationalisation; move to post-print where feasible |
| **Sachet film (Line 5)** | Custom-printed film; 4-week lead time | Cannot react quickly to promotional pack changes | Plan changes 6+ weeks ahead |
| **Aluminium tubes (Line 4)** | Imported; 6-week lead time | Exposure to import delays and currency risk | Maintain 8-week safety stock |
| **Shrink sleeve labels** | Print lead time 3–4 weeks | Promotional sleeve changes require early commitment | Align sleeve artwork with promotional calendar |

---

## 4. Quality and Regulatory Constraints

| Constraint | Impact | Details |
|---|---|---|
| **QC release hold time** | Delays FG availability by 1–3 days post-production | Microbiological and stability testing required before release |
| **Mandatory stability studies for formula changes** | 6–12 month lead time for formula changes | New or modified formulas require accelerated stability data before production |
| **Regulatory labelling requirements (ASEAN)** | SKU-specific label artwork approval required per country | Multi-country SKUs require country-specific labels; artwork approval can take 4–8 weeks |
| **GMP documentation** | Production cannot start without approved batch manufacturing record | Batch records must be issued by QA before line start |
| **Allergen management** | Cross-contamination risk between fragrance families | Scheduling must respect allergen sequencing rules; dedicated CIP may be required |

---

## 5. People Constraints

| Constraint | Impact | Details |
|---|---|---|
| **Specialist skills for Line 4 (tube filler)** | Limited to 2–3 trained operators per shift | Breakdowns on Line 4 cause extended downtime if specialist operators are absent |
| **QA sign-off dependency** | Production start delayed if QA not available | First-fill sign-off and in-process QA checks require QA presence on shift |
| **Planning knowledge concentration** | Key-person dependency on lead planner | Touchless planning capability building is required to reduce this risk |
| **Shift coverage** | Overtime and agency labour required during peak periods | High-volume periods (Q3/Q4) strain permanent headcount |
| **Training for new equipment / processes** | Downtime during ramp-up of new lines or SKUs | Structured OJT and standard operating procedures required |

---

## 6. Utility and Infrastructure Constraints

| Utility / Infrastructure | Constraint | Impact |
|---|---|---|
| **Steam supply** | Single boiler configuration; planned maintenance requires full shutdown | All mixing and heating operations stop during boiler maintenance |
| **Chilled water** | Chiller capacity limits number of simultaneous cooling cycles | Bulk making throughput limited in peak summer months (higher ambient temperature) |
| **Compressed air** | Pressure drops observed when all lines run simultaneously | Inconsistent air pressure affects capper and filler pneumatics |
| **Purified water (PW)** | PW generation capacity limits CIP throughput | Multiple simultaneous CIPs can deplete PW buffer tank |
| **Finished goods warehouse** | Limited racking capacity during peak production periods | FG despatch must accelerate during high-volume months to avoid warehouse congestion |
| **Cold chain** | No cold storage at plant (ambient storage only) | Restricts product range to ambient-stable formulas only |

---

## 7. Constraint Register

The **Constraint Register** is a living document summarising all known active constraints, their owners, and mitigation status.

| ID | Constraint Description | Category | Severity | Owner | Mitigation Status | Target Resolution |
|---|---|---|---|---|---|---|
| C-001 | Line 1 labeller speed limit on 90 ml format | Capacity | High | Engineering | Under investigation — upgrade options being assessed | Q4 2026 |
| C-002 | Line 3 gear pump seal life | Capacity | High | Engineering | PM frequency increased to every 3 weeks | Ongoing |
| C-003 | Line 4 manual cartoning bottleneck | Capacity | Medium | Production | Auto-cartoner capex proposal under review | Q1 2027 |
| C-004 | Fragrance single-source supply risk | Material | High | Procurement | Dual-source qualification in progress | Q3 2026 |
| C-005 | Sachet film 4-week lead time | Material | Medium | Material Planner | Safety stock increased to 6 weeks | Ongoing |
| C-006 | QC release hold time (1–3 days) | Quality | Medium | QA Manager | Rapid micro test method under validation | Q2 2027 |
| C-007 | Planning key-person dependency | People | Medium | SC Manager | Cross-training programme initiated | Q3 2026 |
| C-008 | Compressed air pressure drops | Utility | Medium | Engineering | Compressed air audit completed; compressor upgrade in capex plan | Q2 2027 |

> **Update frequency:** Constraint Register reviewed monthly as part of the S&OP pre-review.
> See [Action Plans](../08-action-plans/README.md) for linked improvement initiatives.
