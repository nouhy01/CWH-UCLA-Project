# CWH-UCLA-Project: School Greening & Watershed Equity
### Identifying Intersectional Opportunity Sites for Stormwater & Equity

[![UCLA Engineering](https://img.shields.io/badge/UCLA-Civil%20%26%20Environmental-blue)](https://samueli.ucla.edu/)
[![Partner](https://img.shields.io/badge/Partner-Council%20for%20Watershed%20Health-green)](https://www.watershedhealth.org/)
[![DASHBOARD](cwh-dashboard.surge.sh)]
---

## Problem Statement
Public schools in Los Angeles County often lack adequate tree canopy, contributing to "Urban Heat Island" effects that disproportionately impact disadvantaged communities. Simultaneously, LA’s watershed requires more permeable surfaces for stormwater capture. 

This project solves the "Data Fragmentation" problem by merging environmental, hydrological, and socioeconomic datasets into a **Unified School Layer**, allowing groups to prioritize greening projects where they provide the most significant community and environmental ROI.

## Key Objectives
* **Data Centralization**: Integration of CalEnviroScreen 5.0 (Draft), CA Schoolyard Tree Canopy Equity Study, and SCWP planning tools.
* **Equity-First Prioritization**: Ranking schools based on the intersection of environmental burden and socioeconomic vulnerability.
* **Hydrological Mapping**: Identifying "high impermeability + high infiltration" sites to maximize groundwater recharge potential.
* **Active Transportation**: Mapping connectivity between schools and parks.

---


## Data Dictionary & Repository Structure
This repository is organized to separate raw data, processing documentation, and visual analysis.

Files for ArcGIS layers can be downloaded here:
https://drive.google.com/file/d/1Z6dWAoYiOX90I0CmPKkzbGt18-a-DBjL/view?usp=sharing

| Folder / File | Contents & Description |
| :--- | :--- |
| **`/Data/CSNA`** | **Community Strategy Needs Assessment**: Spatial layers (GeoJSON) for community-level opportunity areas and survey responses. |
| **`/Data/Community Characteristics`** | Socioeconomic indicators including `FinalGSA_AGOL_2024.csv`, `HighNeed_AGOL.csv`, and Green Schoolyard categories. |
| **`/Data/School Canopy`** | **Tree Canopy Equity Study**: Contains `school_canopy_data.csv` and resource links for urban heat island analysis. |
| **`/Data/Watershed`** | **Hydrologic Layers**: Groundwater basins, hydrogeologic forebays, major watersheds, and SCWP Watershed Areas (GeoJSON). |
| **`/Documentation`** | Metadata and source tracking, specifically the `Data Sources (Michael's layers)` documentation. |
| **`/Figures`** | **Analytical Suite**: Contains `Plots_For_Project.ipynb` and exported visuals like `Environmental Burden Distribution` and `Poverty vs. Cumulative Impact`. |
| **`/Requirements`** | **Environment Setup**: Lists `Software Dependencies` necessary to replicate the Python environment. |
| **`README.md`** | Project documentation, objectives, and usage instructions. |

---

### Technical Requirements
* **Language**: Python 3.8+
* **Geospatial**: `geopandas`, `shapely`
* **Analysis**: `pandas`, `numpy`
* **Visualization**: `matplotlib`
* **ArcGIS**

## Execution & Reproducibility
The analysis is designed to be fully reproducible.



The code in `Figures/Plots_For_Project.ipynb` is configured to pull the latest data directly from this GitHub repository's `main` branch.

1.  **Clone the repo**: `git clone https://github.com/nouhy01/CWH-UCLA-Project.git`
2.  **Install dependencies**: `pip install -r Requirements/Software_Dependencies.txt`
3.  **Run Analysis**: Open `Plots_For_Project.ipynb` to regenerate all plots.

---

## Expected Outputs (WIP for metrics. Need Further input on what variables we need)
The project generates several key metrics for decision-makers:
* **Heat Vulnerability Index**: Schools with the lowest canopy-to-student ratio.
* **Stormwater Capture Ranking**: Campuses sitting on "high-infiltration" soil types (Forebays).
* **Cumulative Impact Scores**: Schools in the top 10% of CalEnviroScreen burden.

---

## Acknowledgments
* **Nouh J. Sepulveda** – UCLA Undergraduate
* **Michael Adams Jr.** – UCLA Undergraduate
* **Professor Isabella Arzeno-Soltero** – UCLA Civil & Environmental Engineering
* **Council for Watershed Health (CWH)**

---
