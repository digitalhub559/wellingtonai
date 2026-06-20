# HydelAI — Product Context Brief
**Last Updated:** 20 June 2026
**Prepared by:** Wellington Marketers / SS Agency
**Status:** Active Development — R&D Phase · Global Site Simulator added

---

## 1. Product Identity

**Product Name:** HydelAI
**Full Title:** Integrated High-Voltage Collector Network and Intelligent Hydroelectric Dispatch System
**Tagline:** *Use the same water better. Deliver more clean energy without building a single new dam.*
**Internal Platform Reference:** NIHIP (Nilgiris Integrated Hydel Intelligence Platform)

---

## 2. The Problem Being Solved

The Nilgiris Hydroelectric Cascade — comprising Kundah (~585 MW), Pykara (~209 MW), Moyar (~36 MW) and associated assets — currently totals approximately **840 MW of installed hydel capacity**. Despite this, these stations operate as **isolated independent facilities** with:

- No system-wide optimisation
- Station-level dispatch decisions only
- Localised reservoir management
- No common SCADA or Energy Management System
- Transmission losses not minimised at system level
- Annual energy recovery far below what coordinated operation could yield

At a 45% capacity factor the 840 MW system produces approximately **3.31 TWh/year**. Modelling shows that even a 5–15% efficiency improvement through coordinated operation delivers **166–497 GWh of additional energy per year** — equivalent to constructing a new 40–125 MW hydroelectric project, without building a single new dam.

---

## 3. Core Objective

> **Transform the Nilgiris Hydroelectric Cascade from a collection of isolated power stations into a single coordinated, AI-optimised renewable energy fleet.**

Specific goals:
1. Reduce aggregate transmission losses via shared high-voltage collector architecture
2. Dynamically coordinate reservoir releases using real-time optimisation algorithms
3. Centrally manage reactive power support for network efficiency
4. Increase annual recoverable energy through predictive dispatch
5. Deliver reliable grid support to Coimbatore and wider Tamil Nadu network

---

## 4. System Architecture (5-Layer Framework)

```
LAYER 1 — GENERATION
Kundah Complex (~585 MW) | Pykara Complex (~209 MW) | Moyar (~36 MW) | Valparai/Kadamparai (~560 MW)
        ↓
LAYER 2 — COLLECTION
Generator Step-Up Transformers → 400 kV Collector Ring → Central Pooling Station
        ↓
LAYER 3 — CONTROL
SCADA Control Centre | Automatic Generation Control (AGC)
        ↓
LAYER 4 — OPTIMISATION
Predictive Dispatch Algorithms | Reservoir Optimisation | Digital Twin Environment | Carbon Intelligence
        ↓
LAYER 5 — GRID INTEGRATION
Tamil Nadu Grid → Coimbatore Load Centres → Western Tamil Nadu Demand
```

**Collector network options evaluated:**
- Independent station operation (baseline)
- Shared 220 kV collector systems
- Shared 400 kV collector systems *(recommended for Kundah/Pykara cluster)*
- Hybrid architectures

---

## 5. Key Performance Data

### Installed Capacity Reference
| Asset | Capacity | Capacity Factor | Voltage |
|---|---|---|---|
| Kundah Complex | ~585 MW | 0.45 | 220 kV |
| Pykara Complex | ~209 MW | 0.45 | 220 kV |
| Moyar | ~36 MW | 0.45 | Regional grid |
| Valparai/Kadamparai | ~560 MW | 0.40 | 220 kV |
| **Total Nilgiris Hydel** | **~840 MW** | **0.45** | — |

### Annual Energy Scenarios (840 MW reference)
| Capacity Factor | Annual Energy | Conditions |
|---|---|---|
| 35% | 2.58 TWh/yr | Low water / conservative |
| 45% | 3.31 TWh/yr | Moderate (baseline) |
| 55% | 4.05 TWh/yr | Good water + coordination |
| 65% | 4.78 TWh/yr | High utilisation / strong rainfall |

### Optimisation Gain Scenarios
| Scenario | Efficiency Gain | Additional GWh/yr | Revenue @ ₹5/kWh |
|---|---|---|---|
| Base (no change) | 0% | 0 | — |
| SCADA only | 6% | ~199 GWh | ~₹100 Cr/yr |
| Collector Network | 10% | ~331 GWh | ~₹166 Cr/yr |
| Full Optimisation | 15% | ~497 GWh | ~₹249 Cr/yr |

### Equivalent Capacity Value
A 10% optimisation gain on a 3.31 TWh base = ~331 GWh/yr = equivalent to **~84 MW of new hydel capacity** at 45% CF — without constructing a new dam.

---

## 6. Financial Investment Options

| Option | Description | Investment | Payback |
|---|---|---|---|
| A | Optimisation Platform (SCADA + EMS + Digital Twin only) | ₹60–145 Crore | 1–3 Years |
| B | Full Collector Network + Platform | ₹375–925 Crore | 3–6 Years |
| C | Strategic Regional Integration (incl. Valparai cluster) | ₹1,200 Crore | 4–6 Years |

---

## 7. Carbon Intelligence Module

**Methodology:** CO2 Reduction (t/yr) = Additional Energy (kWh) × Grid Emission Factor (0.70 kgCO2/kWh) ÷ 1000

| Scenario | Extra GWh | CO2 Avoided | Value @€50/t | Value @€100/t |
|---|---|---|---|---|
| 5% Gain | 166 | 116,200 t | €5.81 M | €11.62 M |
| 10% Gain | 331 | 231,700 t | €11.58 M | €23.17 M |
| 15% Gain | 497 | 347,900 t | €17.40 M | €34.80 M |

---

## 8. Technological Uncertainties (R&D Foundation)

| TU | Uncertainty |
|---|---|
| TU-01 | Whether multiple hydro assets can coordinate through a common collector network without voltage instability or reactive power imbalances |
| TU-02 | Whether real-time algorithms can simultaneously satisfy grid demand, water availability, environmental flows and transmission constraints |
| TU-03 | Whether the collector-network topology reduces aggregate transmission losses sufficiently to justify deployment |
| TU-04 | Whether predictive dispatch algorithms increase annual recoverable energy through reduced spillage |
| TU-05 | Whether centralised SCADA/EMS can operate effectively across geographically distributed hydel facilities |
| TU-06 | Whether advanced control systems can improve energy recovery without increasing installed capacity |

---

## 9. R&D Phases Completed

| Phase | Activity | Key Output |
|---|---|---|
| 1 | Network Modelling | Power-system models: generators, transformers, collector configs, transmission |
| 2 | Hydro Cascade Modelling | Hydraulic models: reservoir interactions, water-release sequencing, seasonal scenarios |
| 3 | SCADA and EMS Development | Supervisory control, AGC, predictive dispatch algorithms, reservoir optimisation modules |
| 4 | Performance Analysis | Peak demand, low inflow, high renewable penetration, grid disturbance scenarios |

**Key HMRC finding:** Activities extended beyond routine engineering and generated new knowledge not readily deducible at project outset. Qualifies for BEIS R&D Tax Relief.

---

## 10. Development Roadmap (7 Phases)

| Phase | Purpose |
|---|---|
| 1 – Asset Mapping | Map all reservoirs, plants, tunnels, lines, substations and catchments |
| 2 – Data Collection | Rainfall, storage, release, generation and loss data |
| 3 – Energy Model | Calculate MW, GWh, TWh and capacity factor scenarios |
| 4 – Collector Study | Identify where common collector network improves losses |
| 5 – SCADA / Digital Twin | Create operating model for dispatch decisions |
| 6 – Pilot Project | Select one cluster (recommended: Kundah) for trial deployment |
| 7 – Investment Case | Prepare DPR, revenue and payback model |

---

## 11. Coimbatore Demand Context

| Metric | Value |
|---|---|
| Coimbatore Daily Demand | ~60 GWh/day |
| Coimbatore Annual Demand | ~21,900 GWh/yr |
| HydelAI 10% gain support | ~331 GWh → equivalent to ~33 days of Coimbatore demand |

---

## 12. Regional Energy Sources (Coimbatore Grid)

| Source | Role |
|---|---|
| Nilgiris Hydel (HydelAI) | Renewable generation and peak support |
| Valparai / Sholayar / Aliyar | Hydel and water-linked generation support |
| Wind (Coimbatore Region) | Major seasonal renewable (~1,500 MW) |
| Solar | Daytime support |
| Thermal / Grid | Base and balancing support |

---

## 13. Efficiency Improvement Levers (Stacked Gains)

| Measure | Indicative Gain |
|---|---|
| Modern low-loss transformers | 0.2% to 1% |
| Higher transmission voltage | 1% to 5%+ |
| Reactive power optimisation | 0.5% to 3% |
| SCADA dispatch coordination | 1% to 10% |
| Reservoir coordination / spill reduction | Significant in wet years |
| Collector network evacuation | System-dependent |

**Total stacked gain target: 6–15%**

---

## 14. Technical Expertise Required

- Power-system engineering
- Hydroelectric generation
- Electrical transmission design
- SCADA systems development
- Energy Management Systems (EMS)
- Hydraulic modelling
- Control systems engineering
- Digital twin platforms
- AI/ML for predictive dispatch

---

## 15. Key Validation Items (Pre-Investment)

| Item | Validation Required |
|---|---|
| 840 MW system reference | Confirm exact plant-wise installed capacity (TANGEDCO) |
| Capacity factor | Use 10-year generation records |
| Reservoir storage | Use official level-storage curves (PWD/CEA) |
| Transmission loss | Actual line length and load-flow study |
| Revenue | Actual tariff and avoided cost data |
| Coimbatore demand | Use TANGEDCO demand data |
| Valparai linkage | Map actual grid and hydrological connections |

---

## 16. Data Sources (Input Files)

| File | Description |
|---|---|
| `IHVC HMRC R&D Technical Report.pdf` | HMRC R&D qualifying activities report, TU definitions, expenditure categories |
| `Feasibility, Research and Development Report.pdf` | Full feasibility study, system architecture, financial scenarios A/B/C |
| `Global Hydel Project and Sustainability.pdf` | 24-section Nilgiris concept document, layman-to-board narrative, NIHIP carbon module |
| `Advanced_Nilgiris_Coimbatore_Collector_Model.xlsx` | Power sources, collector scenarios, Coimbatore demand, architecture diagram |
| `Global_Hydel_Project_Carbon_Updated.xlsx` | 13-site global model, Nilgiris database entry, 30-year financial model, carbon savings |

---

## 17. Coding / Development Notes for Future Reference

### Platform Architecture
- **Frontend:** Interactive HTML dashboard with scenario modelling
- **Core modules to build:**
  - Energy yield calculator (MW × CF × 8760 × gain%)
  - Transmission loss optimiser (collector topology selector)
  - Reservoir dispatch simulator (water volume × head × efficiency)
  - Carbon savings calculator (GWh × 0.70 kgCO2/kWh)
  - Financial model (CapEx options A/B/C, NPV/IRR/payback)
  - Live dispatch map (Kundah → Pykara → Moyar → collector → grid)

### Key Formulas
```
Annual Energy (MWh) = Installed Capacity (MW) × 8760 × Capacity Factor
Power (MW) = 9.81 × Flow (m³/s) × Head (m) × Efficiency / 1000
CO2 Avoided (t/yr) = Additional Energy (MWh) × 0.70
Revenue (₹Cr/yr) = Additional Energy (GWh) × Tariff (₹/kWh) ÷ 10
Equivalent MW = Annual Gain (MWh) / (8760 × Capacity Factor)
```

### Site-Specific Parameters (Nilgiris Cascade)
```
Flow: 48 m³/s (design reference)
Head: 680 m (Kundah high-head reference)
Turbine Efficiency: 0.89
Capacity Factor: 0.46
Tariff: ₹5.10/kWh
CAPEX: ₹10.80 Cr/MW
CO2 Factor: 0.70 kgCO2/kWh
Project Life: 35 years
```

---

## 18. Global Site Simulator (added 20 June 2026)

A new selector-driven module (`#sec-global`, nav label "Global Sites") extends HydelAI beyond the Nilgiris cascade to a 13-site global hydel feasibility model. Source of truth: `Global_Hydel_Project_Carbon_Updated-2.xlsx`. The simulator reproduces the spreadsheet's Hydel Energy Model + 30-year Financial Model exactly (Canadian Mountain Hydro benchmark matches the workbook to 4 decimals: NPV 237.2864, IRR 8.3853%, CO₂ 903,020 t/yr).

### How it works
The user picks a **site** and a **hydrology scenario**; the engine recomputes capacity, generation, revenue, NPV/IRR, payback, CO₂ avoided, a 30-year discounted cash-flow chart, and a scenario-comparison bar chart.

### Site database (13 sites)
Each `SITES[]` entry carries: name, flag, region, currency unit, design flow Q (m³/s), head H (m), turbine efficiency η, capacity factor CF, tariff, CAPEX per MW, O&M fraction, construction years, asset life, discount rate, transmission CAPEX, royalty, auxiliary load, seasonality, CO₂ grid factor. Sites: Nilgiris Hydro Cascade 🇮🇳, Canadian Mountain Hydro 🇨🇦 (workbook default/benchmark), Valparai/Aliyar 🇮🇳, Bhavani Basin 🇮🇳, Himalayan Run-of-River 🇮🇳, Western Ghats Storage 🇮🇳, Norway Fjord 🇳🇴, Alpine 🇨🇭, Brazil River 🇧🇷, US Small Hydro 🇺🇸, Japan Mountain 🇯🇵, New Zealand 🇳🇿, East Africa Rift 🌍.

### Hydrology scenarios (flow multipliers on design Q)
P90 Dry ×0.65 · P75 Conservative ×0.80 · P50 Base ×1.00 (default) · P25 Wet ×1.15 · P10 High Flow ×1.30 · Maintenance ×0.55. Derived from the workbook's Live Hydel Map Simulation sheet.

### Model formulas (per site, given flow multiplier `mult`)
```
Qa      = Q × mult
MW      = 9.81 × Qa × H × η / 1000
firm MW = MW × (1 − seasonality)
gen GWh = MW × CF × 8760 / 1000
net GWh = gen GWh × (1 − aux)
CO2 t/yr= net MWh × CO2 factor
CAPEX   = (MW × CAPEX/MW) + transmission CAPEX
revenue = net MWh × tariff ÷ currency-scale
opex    = CAPEX × O&M frac + revenue × royalty
payback = CAPEX / (revenue − opex)
NPV     = Σ y=1..life  [rev×1.025^(y-1) − opex×1.035^(y-1)] / (1+disc)^y  − CAPEX
IRR     = rate where NPV = 0 (bisection)
```

### Currency-scaling fix (important)
The workbook's raw revenue formula `MWh × tariff / 1000` is only dimensionally correct for **million-denominated** currencies (CAD m, USD m, etc.). For INR Crore and JPY billion it mis-scales by ×100 / ×1000. The engine applies a unit-aware divisor `SCALE = { Cr: 10000, m: 1000, bn: 1000000 }` keyed off the site currency string. This keeps the Canadian benchmark exact while producing correct figures for Indian sites (Nilgiris ≈ 285 MW, ₹577 Cr/yr revenue, ₹3,218 Cr CAPEX, 6.7-yr payback, 17% IRR).

### Revenue bug fix (Nilgiris Cascade Scenario Modeller)
The pre-existing `calc()` used `rev = gain × tar × 10`, inflating revenue ×100 (showed ₹16.5k Cr/yr). Corrected to `rev = gain × tar ÷ 10` (e.g. 331 GWh × ₹5/kWh ÷ 10 = ₹166 Cr/yr), now consistent with the hero box. Root cause was the wrong formula previously documented in §17 (now fixed to `÷ 10`).

### Implementation notes
- Chart.js 4.4.1 added via CDN; all charts go through the `safeChart()` wrapper (destroys prior instance before re-creating) per the CLAUDE.md convention.
- Two canvases: `chart-dcf` (cumulative discounted cash flow over asset life) and `chart-scen` (NPV across the six hydrology scenarios, `type:'bar'`).
- `initGlobal()` populates the selectors, defaults to Canadian Mountain Hydro / P50 Base, and calls `renderGlobal()`.

---

*This context file should be updated as the product evolves through each development phase. All numbers are discussion-level feasibility estimates and should be validated against TANGEDCO, PWD, CEA and DPR data before investment decisions.*
