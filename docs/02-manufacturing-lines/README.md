# 02 – Manufacturing Lines

> **Last Reviewed:** 2026-06-28
> **Owner:** Production Manager / Engineering Manager

---

## Contents

1. [Line Summary](#1-line-summary)
2. [Line Descriptions](#2-line-descriptions)
3. [Line Capacities](#3-line-capacities)
4. [Equipment List](#4-equipment-list)
5. [Changeover & Cleaning (CIP/COP)](#5-changeover--cleaning-cipcop)

---

## 1. Line Summary

The BKK plant currently operates the following manufacturing (filling/packing) lines:

| Line | Format Focus | Primary Pack Size(s) | Rated Speed (units/hr) | Status |
|---|---|---|---|---|
| **Line 1** | Bottles – Low Viscosity (Shampoo) | 90 ml, 170 ml, 340 ml | 6,000 | Active |
| **Line 2** | Bottles – Low/Medium Viscosity (Shampoo / Conditioner) | 170 ml, 340 ml, 680 ml | 4,800 | Active |
| **Line 3** | Bottles – High Viscosity (Conditioner / Treatment) | 340 ml, 680 ml, 1 L | 3,600 | Active |
| **Line 4** | Tubes – Treatment / Mask | 170 ml, 340 ml | 2,400 | Active |
| **Line 5** | Sachet / Pouch | 10 ml, 20 ml | 15,000 pouches/hr | Active |

> **Note:** Rated speeds are theoretical maximums. Refer to [Line Capacities](#3-line-capacities) for net available capacity after losses.

---

## 2. Line Descriptions

### Line 1 – High-Speed Bottle Line (Shampoo)

- **Primary Products:** Standard and anti-dandruff shampoos in small and mid-size bottles.
- **Fill Technology:** Volumetric piston filler (low-viscosity product).
- **Capping:** Inline rotary capper (disc-top / flip-top closures).
- **Labelling:** Pressure-sensitive self-adhesive labeller (front + back).
- **Coding:** Inkjet date coder (batch number, best-before date).
- **End-of-Line:** Shrink-wrap sleeve applicator + tray former + palletiser.
- **Key Constraints:** Speed limited by labeller accuracy on small (90 ml) format; high changeover time between 90 ml and 340 ml due to tooling change.

### Line 2 – Versatile Bottle Line (Shampoo / Conditioner)

- **Primary Products:** Shampoos and conditioners across mid-size bottles.
- **Fill Technology:** Volumetric piston filler (low-to-medium viscosity).
- **Capping:** Inline screw capper.
- **Labelling:** Pressure-sensitive self-adhesive labeller (wrap-around).
- **Coding:** Laser coder.
- **End-of-Line:** Case packer + palletiser.
- **Key Constraints:** Viscosity changeover (from shampoo to conditioner) requires a full clean; allocated as the swing line for overflow demand.

### Line 3 – Heavy Bottle Line (Conditioner / Treatment)

- **Primary Products:** Conditioners and hair masks in large bottles.
- **Fill Technology:** Gear pump filler (high-viscosity product).
- **Capping:** Inline press-on / screw capper.
- **Labelling:** Pressure-sensitive self-adhesive labeller.
- **Coding:** Thermal transfer coder.
- **End-of-Line:** Case packer + palletiser.
- **Key Constraints:** Frequent stoppages caused by product stringing at nozzle; pump seal maintenance is a recurring issue.

### Line 4 – Tube Line (Treatment / Mask)

- **Primary Products:** Hair treatment masks in aluminium/plastic tubes.
- **Fill Technology:** Tube filler with servo-driven fold-and-seal.
- **Coding:** Hot stamp coder on tube tail.
- **End-of-Line:** Manual cartoning + case packer.
- **Key Constraints:** Manual cartoning is a bottleneck; tube-seal integrity rejections during quality checks.

### Line 5 – Sachet / Pouch Line

- **Primary Products:** Single-use shampoo and conditioner sachets.
- **Fill Technology:** Form-fill-seal (FFS) horizontal pouch machine.
- **Coding:** Inline inkjet coder on pouch.
- **End-of-Line:** Auto-counting + box filling + case packer.
- **Key Constraints:** Film roll changeovers cause significant downtime; machine sensitivity to humidity affecting seal quality.

---

## 3. Line Capacities

### Theoretical vs. Net Available Capacity

Capacity is calculated based on a standard 3-shift, 24-hour operating day, 5 operating days per week.

| Line | Rated Speed (units/hr) | Theoretical Daily Capacity | Target OEE | Net Available Capacity (units/day) | Net Available Capacity (units/week) |
|---|---|---|---|---|---|
| Line 1 | 6,000 | 144,000 | 75% | 108,000 | 540,000 |
| Line 2 | 4,800 | 115,200 | 75% | 86,400 | 432,000 |
| Line 3 | 3,600 | 86,400 | 72% | 62,208 | 311,040 |
| Line 4 | 2,400 | 57,600 | 68% | 39,168 | 195,840 |
| Line 5 | 15,000 | 360,000 | 70% | 252,000 | 1,260,000 |

> **Note:** OEE targets are reviewed annually. Actual OEE by line is tracked in [Operational Losses](../06-operational-losses/README.md).

### Capacity Conversion to Cases

Pack sizes and case pack quantities vary by SKU. Standard conversion factors are maintained in the Planning Master Data (SAP PP). Representative examples:

| Pack Size | Units per Case | Line 1 Capacity (cases/day) | Line 2 Capacity (cases/day) |
|---|---|---|---|
| 90 ml | 48 | 2,250 | — |
| 170 ml | 24 | 4,500 | 3,600 |
| 340 ml | 12 | 9,000 | 7,200 |
| 680 ml | 6 | — | 14,400 |

---

## 4. Equipment List

Key equipment on each line is listed below. Full asset registers are maintained in the CMMS (Computerised Maintenance Management System).

| Asset Tag | Equipment Description | Line | Make/Model | Install Year | Criticality |
|---|---|---|---|---|---|
| BKK-L1-F01 | Volumetric Piston Filler | Line 1 | *(to be filled)* | *(to be filled)* | Critical |
| BKK-L1-C01 | Rotary Capper | Line 1 | *(to be filled)* | *(to be filled)* | Critical |
| BKK-L1-L01 | Self-Adhesive Labeller | Line 1 | *(to be filled)* | *(to be filled)* | High |
| BKK-L2-F01 | Volumetric Piston Filler | Line 2 | *(to be filled)* | *(to be filled)* | Critical |
| BKK-L3-F01 | Gear Pump Filler | Line 3 | *(to be filled)* | *(to be filled)* | Critical |
| BKK-L4-TF01 | Tube Filler | Line 4 | *(to be filled)* | *(to be filled)* | Critical |
| BKK-L5-FFS01 | Form-Fill-Seal Machine | Line 5 | *(to be filled)* | *(to be filled)* | Critical |

> **Action:** Engineering team to populate asset tags, make/model, and installation year from the CMMS.

---

## 5. Changeover & Cleaning (CIP/COP)

### Changeover Categories

| Type | Description | Typical Duration |
|---|---|---|
| **Size changeover** | Same product formula, different pack size (format parts change only) | 1–2 hours |
| **Colour changeover** | Different product, same viscosity/formula family (rinse required) | 2–3 hours |
| **Full product changeover** | Different viscosity family (e.g., shampoo to conditioner) — full CIP required | 3–5 hours |
| **Tube-to-bottle** | Switching between tube line and bottle line equipment (not applicable in standard operation) | N/A |

### CIP/COP Protocol Summary

1. **Flush** with hot water to remove bulk product residue.
2. **CIP wash** with approved detergent solution (concentration and contact time per SOP QA-CIP-001).
3. **Rinse** with purified water to conductivity ≤ 5 µS/cm.
4. **Swab testing** (where required by quality plan) before next product.
5. **Setup & verification:** Format parts installed, first-fill sample taken for QA sign-off.

> **Note:** Changeover time data is captured in the line logbook and in SAP via process orders. Reduction of changeover time is a key action plan item — see [Action Plans](../08-action-plans/README.md).
