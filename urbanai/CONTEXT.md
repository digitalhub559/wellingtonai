# UrbanAI — Tool Context
> Read before working on UrbanAI. Update after significant changes.

## Tool Name
UrbanAI

## What It Does
Global urban flood resilience intelligence platform. Models adaptive multi-layer infrastructure strategies for extreme rainfall events across 14 global cities. Inputs: city selection + rainfall scenario. Outputs: flood volume, hub clearance time, infrastructure layer activation plan, pump type optimisation, 30-year financial model (CAPEX/NPV/IRR), and resilience score.

## Main File
`urbanai/index.html` — single self-contained HTML file. No build step.

## R&D Objective
Research and Development of an Adaptive Multi-Layer Urban Flood Resilience Infrastructure System for Extreme Rainfall Events. HMRC qualifying R&D — technical report already prepared (UI HMRC R&D Technical Report.pdf).

## Architecture — Five Computation Layers

| Layer | Name | What It Does |
|-------|------|-------------|
| L1 | Rainfall Volume | Converts city area + rainfall scenario to total floodwater volume in m³ |
| L2 | Hub vs Distributed Clearance | Computes ward hub clearance hours vs random pump comparison; calculates clearance saving % and resilience score |
| L3 | Infrastructure Layer Activation | Adaptively selects which of 4 drainage layers to activate based on rainfall intensity |
| L4 | Pump Type Optimisation | Calculates optimal mix of 4 pump types (1.5hp/10hp/25hp/100hp) per hub to meet capacity target |
| L5 | Financial Analysis | 30-year NPV/IRR, CAPEX breakdown, annual net benefit, payback, investment recommendation |

## City Database — 14 Global Cities

| City | Currency | Population | Area km² | Wards | Base Rainfall cm |
|------|----------|-----------|----------|-------|-----------------|
| Coimbatore | INR Cr | 2.5m | 257 | 100 | 70 |
| Chennai | INR Cr | 11.5m | 1189 | 200 | 55 |
| Mumbai | INR Cr | 20.9m | 603 | 227 | 45 |
| Delhi | INR Cr | 32m | 1484 | 272 | 35 |
| Bengaluru | INR Cr | 13.6m | 741 | 198 | 30 |
| Hyderabad | INR Cr | 10.8m | 650 | 150 | 32 |
| London | GBP m | 9.7m | 1572 | 33 | 6 |
| Amsterdam | EUR m | 1.2m | 219 | 8 | 8 |
| New York | USD m | 19.6m | 1214 | 59 | 13 |
| Singapore | SGD m | 5.9m | 734 | 55 | 15 |
| Dubai | AED m | 3.7m | 4114 | 15 | 5 |
| Tokyo | JPY bn | 37.2m | 2194 | 62 | 18 |
| Jakarta | IDR bn | 32.6m | 661 | 44 | 20 |
| Bangkok | THB m | 11.2m | 1569 | 50 | 18 |

## Rainfall Scenarios — 6 Levels

| Scenario | Multiplier | Risk Level |
|----------|-----------|------------|
| Light | 0.35 | Low |
| Design Storm | 1.0 | Medium |
| Severe | 1.4 | High |
| Extreme | 1.8 | Critical |
| Climate Stress | 2.2 | Critical |
| Monsoon Peak | 1.6 | High |

## Infrastructure Layers — 4 Types (Chennai System Design, generalised globally)

| Layer | Type | Activation Threshold |
|-------|------|---------------------|
| Layer 1 | Sequential lake/pond drainage — order-of-flow discharge | Always active |
| Layer 2 | Circular underground flow + artificial storage pumping | Design Storm+ (mult ≥ 1.0) |
| Layer 3 | Unidirectional canal flow (outskirts / sea connection) | Severe+ (mult ≥ 1.4) |
| Layer 4 | Emergency longest-flow sea discharge pathway | Extreme+ (mult ≥ 1.8) |

## Pump Type Mix — 4 Types (from Urban Planning document)

| Type | HP | Capacity |
|------|-----|---------|
| Type A | 1.5 hp | 30 m³/hr (500 lpm) |
| Type B | 10 hp | 36 m³/hr (620 lpm) |
| Type C | 25 hp | 60 m³/hr (1,000 lpm) |
| Type D | 100 hp | 130 m³/hr (2,000 lpm) |

Hub capacity is achieved through a mix of all four types:
40% TypeD + 30% TypeC + 20% TypeB + 10% TypeA (by capacity contribution)

## Key Formulas

| Formula | Expression |
|---------|-----------|
| Floodwater Volume | `(rainfall_cm / 100) × area_km² × 1,000,000 × runoff × scenario_multiplier` |
| Total Hub Capacity | `hubCount × hubCapacity_m³hr` |
| Post-Storage Volume | `MAX(0, volume − storage_m³)` |
| Hub Clearance | `postStorage / totalHubCapacity` (hours) |
| Random Clearance | `volume / (randomPumps × randomPumpCapacity)` (hours) |
| Clearance Saving | `1 − hubClearance / randomClearance` |
| CAPEX | `(hubs × capexPerHub + SCADA + canalWorks) × (1 + contingency)` |
| Net Benefit / yr | `grossDamageAvoided × riskReduction − OPEX` |
| Simple Payback | `CAPEX / annualNetBenefit` |

## Resilience Score (0–100)

Composite of four sub-scores, weighted:
- Hub Clearance Speed: `MAX(0, 100 − hubClearanceHours × 10)` — weight 30%
- Storage Efficiency: `MIN(100, (storage / volume) × 100)` — weight 20%
- Clearance Saving vs Random: `clearanceSaving × 100` — weight 25%
- City Risk Reduction: `riskReduction × 100` — weight 25%

Bands: Vulnerable (0–25) | Moderate (26–50) | Resilient (51–75) | Highly Resilient (76–100)

## Investment Rating Logic

Based on 30-year NPV and Simple Payback:
- Payback < 5 years + NPV > 0: **Excellent** — strong rollout candidate
- Payback 5–10 years + NPV > 0: **Strong** — recommended with phased rollout
- Payback 10–15 years + NPV > 0: **Moderate** — viable with government co-funding
- Payback > 15 years or NPV < 0: **Marginal** — review assumptions and procurement

## UI Tabs
1. **City Intelligence** — City selector (14 cities), rainfall scenario, city overview KPIs
2. **Flood Simulation** — Volume, storage buffer, hub clearance vs random clearance, resilience score gauge
3. **Infrastructure Layers** — 4 adaptive layers with live activation status, pump mix optimisation table
4. **Financial Model** — CAPEX breakdown donut chart, 30-year NPV line chart, IRR, investment recommendation
5. **Urban Map** — SVG schematic: ward grid, pump hubs, storage nodes, canal network, flood risk heat map

## Grant Status
- UK R&D Tax Credit: HMRC technical report prepared (UI HMRC R&D Technical Report.pdf) — awaiting submission
- R&D claim: 5 technological uncertainties — integrated hydraulic behaviour, adaptive pumping architecture, artificial storage optimisation, multi-directional flow control, system resilience during extreme events

## HMRC Field of Technology
**Primary**: Civil Engineering — Adaptive Hydraulic Infrastructure Systems Integration
**Secondary**: Applied Computer Science — Real-Time Urban Flood Simulation and Investment Intelligence

## Source Files
- `Global_Urban_Infrastructure_Flood_Pumping_Model_with_Live_Map.xlsx` — 14-city database, computation formulas, 30-year financial model, architecture map, live flood map simulation
- `Flood_Project_Input_Output_Model.xlsx` — simplified I/O model, cost comparison (215k pumps vs 100 smart hubs), ROI
- `Urban plan, Infrastructure and Systems.pdf` — Chennai system design, 4-layer architecture, pump calculations, project value estimates
- `UI HMRC R&D Technical Report.pdf` — HMRC R&D qualifying report (9 sections, 5 uncertainties)

## Key Files
- `urbanai/index.html` — main platform (single-file HTML)
- `urbanai/CONTEXT.md` — this file

## Last Updated
June 2026
