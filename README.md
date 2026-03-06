# CWH-UCLA-Project: School Greening & Watershed Equity
### Identifying Intersectional Opportunity Sites for Stormwater & Equity

[![UCLA Engineering](https://img.shields.io/badge/UCLA-Civil%20%26%20Environmental-blue)](https://samueli.ucla.edu/)
[![Partner](https://img.shields.io/badge/Partner-Council%20for%20Watershed%20Health-green)](https://www.watershedhealth.org/)

---

### 🔗 [Access the Live Dashboard Here](https://cwh-dashboard.surge.sh/)

# CWH School Greening Priority Dashboard

This repository contains the data, analysis, and ArcGIS project used to create the **CWH School Greening Priority Dashboard**, an interactive map designed to help identify which public schools in **Los Angeles County** should be prioritized for school greening investments.

School greening strategies such as tree planting, shade infrastructure, permeable pavement, and bioswales can reduce urban heat, improve stormwater infiltration, and create healthier environments for students.

The dashboard ranks schools using a **multi-factor greening priority score** and allows users to explore environmental and social indicators that influence greening opportunities.

---

# Final Product

The final product is an **interactive web map dashboard** that allows users to:

- View greening priority rankings for schools
- Explore environmental and socio-economic indicators
- Compare schools across Los Angeles County
- Identify campuses with the highest potential for greening interventions

Users can interact with the dashboard by toggling layers, clicking schools for detailed information, and examining different environmental datasets.

---

# Accessing the Dashboard

The dashboard can be accessed directly online:

**Dashboard Website**

Users can open the website and immediately explore the map. No software or technical knowledge is required.

The map allows users to:
- toggle different environmental layers
- explore school data
- view greening priority rankings
- examine the environmental conditions surrounding each school

---

# Downloading the Data and ArcGIS Project

All project files are available in this repository.

A compressed archive containing the **ArcGIS Pro project and geospatial datasets** is available on the front page of the repository.

To open the full project:

1. Download the `.7z` file from the repository.
2. Extract the archive.
3. Open the `.aprx` file using **ArcGIS Pro**.
4. All layers, maps, and analysis tools will load automatically.

---

# Greening Priority Score

Schools are ranked using a **weighted scoring system** designed to identify campuses where greening interventions could provide the greatest benefit.

The score combines environmental conditions, social vulnerability, and infrastructure opportunities.

### Default Weights

| Category | Weight |
|--------|--------|
Heat & Canopy | 30%
Stormwater Infiltration Potential | 25%
Disadvantaged Community Score | 25%
Parks within ½ mile | 10%
Parks within ¼ mile | 5%
Elementary School Indicator | 5%

These weights were determined in consultation with the **Council for Watershed Health** and can be modified within the dashboard.

---

# Score Components

### Heat & Canopy

Measures how much shade currently exists on school campuses and the potential for reducing heat exposure.

Indicators include:

- Tree canopy coverage
- Surface temperature indicators
- Tree equity metrics

Schools with **low canopy coverage and high heat exposure** receive higher priority.

---

### Stormwater Infiltration Potential

Estimates how much stormwater could be captured or absorbed if greening infrastructure were installed.

This score combines:

- Soil infiltration capacity
- Impervious surface area
- Campus footprint size

Schools with **large impervious areas and favorable soil conditions** receive higher scores.

---

### Disadvantaged Community Score

Socio-economic vulnerability is measured using:

- **CalEnviroScreen 5.0**
- Poverty percentiles

Schools located in communities experiencing **higher pollution burdens and socio-economic disadvantage** receive higher priority.

---

### Park Connectivity

Access to nearby green space is included as a secondary factor.

Metrics include:

- parks within ½ mile
- parks within ¼ mile

Schools with **less nearby park access** receive higher priority.

---

# Data Sources

Major datasets used in the analysis include:

- CalEnviroScreen 5.0
- Tree Equity Scores
- SCWP Opportunity Zones
- Soil data (gNATSGO)
- Watershed boundaries
- School campus footprints
- Park locations

These datasets were combined within **ArcGIS Pro** to produce the final suitability ranking.

---

# How to Use the Dashboard

The dashboard is designed to be simple to use.

Users can:

### Toggle Data Layers
Turn environmental datasets on or off to view different conditions across Los Angeles County.

### Click on Schools
Clicking a school opens a data card showing:

- greening priority score
- canopy coverage
- stormwater potential
- surrounding environmental indicators

### Explore Rankings
The map colors schools based on their greening priority score, allowing users to quickly identify high-priority locations.

---

# Limitations

Several limitations should be considered when interpreting the results.

### Data Resolution
Some datasets are available only at the **census tract level**, which may not perfectly represent conditions at individual schools.

### Canopy Measurement
Tree canopy estimates are derived from satellite imagery and may include classification error.

### Physical Site Constraints
Campus area is used as a proxy for greening potential, but some spaces may be unavailable due to infrastructure such as buildings, athletic courts, or utilities.

---

## Repository Structure
icpms_project/
├── Data/
│   ├── Community Characteristics/
│   │   ├── FinalGSA_AGOL_2024.csv
│   │   ├── Lower LA River Revitalization Plan
│   │   ├── ces.geojson
│   │   └── tree_equity.geojson
│   │
│   ├── SCWP Layer/
│   │   ├── scw_groundwater.geojson
│   │   ├── scw_stormwater.geojson
│   │   ├── scw_waterquality.geojson
│   │   └── watershed_boundaries.geojson
│   │
│   ├── Schools/
│   │   ├── countywide_parks.geojson
│   │   ├── finalschoolswithdatareal.geojson
│   │   └── mupolygon.geojson
│   │
│   └── Watershed/
│       ├── Groundwater basins.geojson
│       ├── Hydrogeologic forebays.geojson
│       ├── Major_Watersheds_in_Los_Angeles.geojson
│       └── Watersheds subbasins.geojson
│
├── Figures/
│   ├── Environmental Burden Distribution
│   ├── Plots_For_Project.ipynb
│   └── Poverty vs. Cumulative Impact
│
├── Requirements/
│   └── Software Dependencies
│
└── README.md
---

# About This Project

This project was created as part of a collaboration with the **Council for Watershed Health** to support data-driven planning for school greening initiatives across Los Angeles County.

The goal is to provide an accessible tool that helps identify locations where greening investments can produce the greatest environmental and community benefits.
