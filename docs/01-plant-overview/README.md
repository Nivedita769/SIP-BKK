# 01 – Plant Overview

> **Last Reviewed:** 2026-06-28
> **Owner:** Plant Management Team

---

## Contents

1. [Facility Summary](#1-facility-summary)
2. [Product Portfolio](#2-product-portfolio)
3. [Plant Layout](#3-plant-layout)
4. [Organizational Structure](#4-organizational-structure)
5. [Key Performance Indicators (KPIs)](#5-key-performance-indicators-kpis)

---

## 1. Facility Summary

| Attribute | Details |
|---|---|
| **Plant Name** | BKK Hair Care Plant |
| **Site Code** | BKK |
| **Location** | Bangkok, Thailand |
| **Category** | Hair Care (Shampoo, Conditioner, Treatment) |
| **Operating Model** | Make-to-Stock (MTS) / Make-to-Order (MTO) |
| **Operating Hours** | 3 shifts × 8 hours = 24 hours/day, 5–7 days/week |
| **Total Headcount** | *(to be filled)* |
| **GMP Certification** | ISO 22716 – Good Manufacturing Practices for Cosmetics |

---

## 2. Product Portfolio

The BKK plant produces a range of hair care products across multiple formats and pack sizes.

| Product Category | Sub-Category | Pack Formats | Volume Range |
|---|---|---|---|
| Shampoo | Standard, Anti-Dandruff, Moisturising | 90 ml, 170 ml, 340 ml, 680 ml, 1 L | High |
| Conditioner | Rinse-Off, Leave-In | 90 ml, 170 ml, 340 ml, 680 ml | Medium |
| Hair Treatment | Mask, Serum, Oil | 170 ml, 340 ml | Low-Medium |
| Specialist Range | Colour Care, Repair | 170 ml, 340 ml | Low |

> **Note:** SKU count and exact formulations are maintained in the Product Master (SAP Material Master).

---

## 3. Plant Layout

```
┌─────────────────────────────────────────────────────────────────────┐
│                        BKK HAIR CARE PLANT                          │
│                                                                     │
│  ┌──────────────┐   ┌──────────────────────────────────────────┐   │
│  │  Raw Material │   │           MANUFACTURING AREA             │   │
│  │  Warehouse    │   │  ┌──────────┐  ┌──────────┐             │   │
│  │  (RM Store)   │──▶│  │  Line 1  │  │  Line 2  │   ...       │   │
│  └──────────────┘   │  │ (Filling)│  │ (Filling)│             │   │
│                     │  └──────────┘  └──────────┘             │   │
│  ┌──────────────┐   │                                          │   │
│  │  Bulk Making  │──▶│  ┌──────────────────────────────────┐  │   │
│  │  (Mixing)     │   │  │         PACKING / LABELLING       │  │   │
│  └──────────────┘   │  └──────────────────────────────────┘  │   │
│                     └──────────────────────────────────────────┘   │
│                                     │                               │
│                     ┌───────────────▼────────────────┐             │
│                     │     Finished Goods Warehouse    │             │
│                     │     (FG Store / Dispatch)        │             │
│                     └────────────────────────────────┘             │
└─────────────────────────────────────────────────────────────────────┘
```

> **Note:** A detailed CAD layout drawing is maintained separately. The schematic above is for orientation purposes only.

### Key Areas

| Area | Function |
|---|---|
| **Raw Material Warehouse** | Receipt, sampling, and storage of raw materials (actives, excipients) and packaging materials |
| **Bulk Making (Mixing)** | Weighing, blending, heating/cooling of bulk formula batches |
| **Manufacturing Lines (Filling)** | Filling, capping, labelling, and coding of finished product |
| **Quality Control Lab** | In-process and release testing |
| **Finished Goods Warehouse** | Storage and outbound dispatch of finished goods |
| **Utilities Room** | Boilers, compressed air, chilled water, and HVAC systems |

---

## 4. Organizational Structure

```
Plant Manager
│
├── Production Manager
│   ├── Shift Manager (A / B / C)
│   │   └── Line Operators, Technicians
│   └── Bulk Making Supervisor
│       └── Mixing Operators
│
├── Engineering & Maintenance Manager
│   ├── Mechanical Maintenance Team
│   └── Electrical / Automation Team
│
├── Quality Assurance Manager
│   ├── QC Lab Team
│   └── QA Compliance Team
│
├── Supply Chain / Planning Manager
│   ├── Production Planning
│   └── Warehouse & Logistics
│
└── EHS Manager
```

> **Note:** Headcount per function and names of role holders are maintained in the HR system. Update this structure when significant org changes occur.

---

## 5. Key Performance Indicators (KPIs)

These are the plant-level KPIs tracked and reported on a daily/weekly/monthly basis.

| KPI | Definition | Target | Frequency |
|---|---|---|---|
| **OEE** | Overall Equipment Effectiveness (Availability × Performance × Quality) | ≥ 75% | Daily |
| **Volume Attainment** | Actual production vs. plan (cases or units) | ≥ 98% | Daily |
| **Plan Adherence** | % of planned orders completed on time | ≥ 95% | Weekly |
| **Right First Time (RFT)** | Batches / lots released without rework | ≥ 99% | Weekly |
| **Waste / Loss %** | Material loss as % of theoretical yield | ≤ 1.5% | Monthly |
| **Schedule Attainment** | % of master schedule completed | ≥ 95% | Weekly |
| **Changeover Time** | Average time to change between SKUs (minutes) | *(target per line)* | Per event |
| **OTIF (Outbound)** | On-Time In-Full delivery to distribution | ≥ 98% | Weekly |

See [Production Volumes](../03-production-volumes/README.md) for historical KPI data.
