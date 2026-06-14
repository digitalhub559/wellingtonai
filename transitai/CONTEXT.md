# TransitAI — Full Design Brief

> Wellington AI Tool 4. Read this before working on `transitai/index.html`.

## Overview

**TransitAI** is a Climate-Positive European-Style Urban Mobility Ecosystem Intelligence Platform developed specifically for Coimbatore City, benchmarked against 17 global tram networks across India, Europe, Americas, and Asia-Pacific.

**R&D Objective (from ESUM MRC R&D Technical Report):**
> "Development of a Climate-Positive European-Style Urban Mobility Ecosystem Integrating Renewable Energy Collector Networks, AI-Driven Tram Operations and Digital Twin-Based Transit-Oriented Development for Coimbatore City"

---

## Main File

`transitai/index.html` — single-file HTML app (~1,400 lines)

---

## Five R&D Uncertainties (from Technical Report)

1. **Renewable Energy Integration** — Nilgiris hydro-powered collector network optimisation
2. **AI-Based Passenger Prediction** — ML demand forecasting for headway adjustment
3. **Digital Twin Urban Simulation** — real-time city model for transit-oriented development
4. **Collector Network Optimisation** — pantograph + overhead wire efficiency vs battery storage
5. **Climate-Positive Transport Operation** — net-negative carbon lifecycle including embedded energy

---

## Five R&D Phases

1. Demand Analysis & corridor identification (4 Coimbatore routes)
2. Tram Corridor Engineering (geometry, grade, turning radius)
3. Renewable Energy Modelling (Nilgiris hydro, solar rooftop, grid)
4. Digital Twin Development (city-scale simulation environment)
5. AI Optimisation Research (fleet scheduling, passenger load prediction)

---

## UI Structure — 5 Tabs

| Tab | Name | Content |
|-----|------|---------|
| 1 | City Intelligence | City selector (18 cities, grouped), scenario pills, KPI dashboard, revenue vs OPEX chart |
| 2 | Operations Model | Fleet computation, cycle time, headway analysis, fleet doughnut chart |
| 3 | Financial Model | CAPEX breakdown doughnut, 30-yr NPV line chart, IRR, payback period |
| 4 | Sustainability Impact | Modal shift, CO2 reduction, fuel savings, renewable energy %, sustainability bar chart |
| 5 | Live Tram Map | SVG map — Coimbatore 4 routes with all stops; schematic for other cities |

---

## Colour Theme

- **Primary navy**: `#1F3864` (Wellington AI brand)
- **Climate green**: `#16A34A`
- **Mid green**: `#059669`
- **Light green bg**: `#DCFCE7`
- **Tab active**: green (`#16A34A`)
- Font: Arial

---

## 18-City Database

### Indian Cities (6)

| City | Pop (M) | Route km | Riders/day | Fare | CAPEX/km (Cr) | OPEX/km/yr (Cr) | Disc% |
|------|---------|----------|------------|------|---------------|-----------------|-------|
| Coimbatore | 2.5 | 75 | 350,000 | ₹20 | 75 | 2.4 | 10% |
| Chennai | 11.5 | 120 | 900,000 | ₹25 | 95 | 3.0 | 10% |
| Bengaluru | 13 | 110 | 850,000 | ₹28 | 100 | 3.2 | 10% |
| Hyderabad | 10.5 | 105 | 750,000 | ₹27 | 92 | 2.9 | 10% |
| Mumbai | 21 | 140 | 1,500,000 | ₹30 | 120 | 3.8 | 9% |
| Delhi | 32 | 160 | 1,700,000 | ₹30 | 115 | 3.6 | 9% |

Currency: INR Cr | Scale: ÷10,000,000

### European Cities (6)

| City | Pop (M) | Route km | Riders/day | Fare | CAPEX/km | OPEX/km/yr | Disc% |
|------|---------|----------|------------|------|----------|------------|-------|
| London | 9 | 150 | 900,000 | £2.8 | £90m | £2.1m | 8% |
| Manchester | 2.8 | 100 | 450,000 | £2.2 | £70m | £1.6m | 8% |
| Paris | 11 | 180 | 1,200,000 | €2.3 | €95m | €2.2m | 7% |
| Amsterdam | 1.2 | 85 | 420,000 | €2.1 | €75m | €1.7m | 7% |
| Berlin | 3.7 | 130 | 650,000 | €2.4 | €80m | €1.8m | 7% |
| Madrid | 6.7 | 115 | 520,000 | €1.8 | €75m | €1.5m | 7% |

UK: GBP m (÷1,000,000) | Euro: EUR m (÷1,000,000)

### Americas (2)

| City | Pop (M) | Route km | Riders/day | Fare | CAPEX/km | OPEX/km/yr | Disc% |
|------|---------|----------|------------|------|----------|------------|-------|
| New York | 8.5 | 200 | 1,500,000 | $3.0 | $110m | $2.8m | 8% |
| Toronto | 6.3 | 120 | 700,000 | C$3.2 | C$95m | C$2.4m | 7% |

### Asia-Pacific (4)

| City | Pop (M) | Route km | Riders/day | Fare | CAPEX/km | OPEX/km/yr | Disc% |
|------|---------|----------|------------|------|----------|------------|-------|
| Melbourne | 5.2 | 150 | 800,000 | A$4.6 | A$85m | A$2.2m | 7% |
| Sydney | 5.3 | 120 | 650,000 | A$4.0 | A$95m | A$2.4m | 7% |
| Singapore | 5.6 | 100 | 650,000 | S$2.1 | S$70m | S$1.5m | 7% |
| Dubai | 3.6 | 90 | 520,000 | AED4 | AED85m | AED1.8m | 7% |

---

## Scenario Multipliers

| Scenario | Rider Factor | CAPEX Factor | OPEX Factor |
|----------|-------------|--------------|-------------|
| Conservative | 0.85 | 1.10 | 1.05 |
| Base | 1.00 | 1.00 | 1.00 |
| Optimistic | 1.15 | 0.95 | 0.95 |

---

## Computation Engine — Key Formulas

### Operations Model
```
oneWayTime (min) = routeKm / commercialSpeed × 60
cycleTime (min)  = 2 × oneWayTime + 10  [terminal dwell]
activeFleet      = ceil(cycleTime / headway)
reserveFleet     = ceil(activeFleet × reservePct)
totalFleet       = activeFleet + reserveFleet
peakCapacity     = (60 / headway) × tramCapacity  [pphpd]
```

### CAPEX Model
```
routeInfra    = routeKm × capexPerKm × capexFactor
fleetCost     = totalFleet × tramUnitCost
landUtilities = 12% × routeInfra
subtotal      = routeInfra + fleetCost + landUtilities
contingency   = 12% × subtotal
totalCapex    = subtotal + contingency
```

### Revenue Model
```
fareRevenue   = adjRidershipDay × fare × 365 / currencyScale
totalRevenue  = fareRevenue + adRevenue
annualOPEX    = routeKm × opexPerKm × opexFactor
surplus       = totalRevenue − annualOPEX
```

### 30-Year NPV / IRR
```
CF[0]   = −totalCapex
CF[t]   = surplus × (1 + growthRate)^(t−1)   for t = 1..30
NPV     = Σ CF[t] / (1 + discountRate)^t
IRR     = bisection algorithm [lo=−0.5, hi=5.0, 100 iterations]
Payback = year when cumulative CF crosses zero
```

### Sustainability Metrics
```
vehiclesRemoved/day = adjRidershipDay × 0.065
carsRemoved         = vehiclesRemoved × 0.214
twoWheelersRemoved  = vehiclesRemoved × 0.786
co2PerYear (t)      = carsRemoved × 2.3 + twoWheelersRemoved × 0.5
annualFuelSavings   = vehiclesRemoved × fuelCostPerVehicleMonth × 12 / currencyScale
```

Calibration (Coimbatore Base): 350k riders × 0.065 = 22,750 vehicles → 4,869 cars + 17,882 two-wheelers ≈ 5,000 + 18,000 (Excel data match ✓)

---

## Coimbatore-Specific Details

### 4 Tram Routes (from Europe Tram.xlsx)

**Route 1 — South Corridor** (Blue)
Airport → Avinashi Road → Peelamedu → Gandhipuram → Railway Station → Ukkadam

**Route 2 — North/IT Corridor** (Green)
Airport → IT Corridor (Tidel/Kalapatti) → Saravanampatti → Neelambur

**Route 3 — West Corridor** (Orange)
Gandhipuram → RS Puram → Thondamuthur → Madukkarai → Kuniyamuthur → Ukkadam

**Route 4 — East Corridor** (Red)
Railway Station → Singanallur → Ondipudur → Eachanari → Vellalore

### Capacity Targets
- 6,000 passengers/day per tram; 15 trips/day per tram
- 100 two-wheelers + 200 bus passengers modal shift per trip
- 18,000 two-wheelers off road/day; 5,000 cars off road/day
- ₹15 crore/month fuel savings to city economy

### Education Catchment
- 10 colleges × 30,000 students
- 20 schools × 60,000 students
- 5 colleges × 15,000 students

### Renewable Energy
- **78%** of tram energy from Nilgiris hydro (renewable)
- Digital Twin integration: real-time city simulation
- Climate-positive lifecycle (net-negative carbon with renewable energy)

---

## Grant & HMRC Status

- **Tool 4 — Planning stage** (no grant yet applied)
- Suitable for HMRC R&D Tax Credit (same claim as EmployAI, TradeAI, UrbanAI)
- R&D Technical Report prepared: "ESUM MRC R&D Technical Report-2.pdf"
- Suitable for Innovate UK Smart Grant (apply after TradeAI round)
- NSF SBIR: requires US C-Corp first (see CLAUDE.md)

---

## Last Updated

June 2026

## Files

```
transitai/
├── CONTEXT.md        ← this file
└── index.html        ← TransitAI platform (18 cities, 5 tabs, 30-yr financial model)
```
