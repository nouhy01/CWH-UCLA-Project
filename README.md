# CWH-UCLA-Project: School Greening & Watershed Equity
### Identifying Intersectional Opportunity Sites for Stormwater & Equity

[![UCLA Engineering](https://img.shields.io/badge/UCLA-Civil%20%26%20Environmental-blue)](https://samueli.ucla.edu/)
[![Partner](https://img.shields.io/badge/Partner-Council%20for%20Watershed%20Health-green)](https://www.watershedhealth.org/)

---

## Problem Statement
Public schools in Los Angeles County often lack adequate tree canopy, contributing to "Urban Heat Island" effects that disproportionately impact disadvantaged communities. Simultaneously, LA’s watershed requires more permeable surfaces for stormwater capture. 

This project solves the "Data Fragmentation" problem by merging environmental, hydrological, and socioeconomic datasets into a **Unified School Layer**, allowing stakeholders to prioritize greening projects where they provide the most significant community and environmental ROI.

## Key Objectives
* **Data Centralization**: Integration of CalEnviroScreen 4.0, CA Schoolyard Tree Canopy Equity Study, and SCWP planning tools.
* **Equity-First Prioritization**: Ranking schools based on the intersection of environmental burden and socioeconomic vulnerability.
* **Hydrological Mapping**: Identifying "high impermeability + high infiltration" sites to maximize groundwater recharge potential.
* **Active Transportation**: Mapping connectivity between schools, parks, and protected bike lanes.

---

## Data Dictionary & Repository Structure
This repository is organized to separate raw data, processing documentation, and visual analysis.

| Folder | Contents |
| :--- | :--- |
| **`/Data/CSNA`** | Community Strategy Needs Assessment: Spatial layers for community-level opportunity areas. |
| **`/Data/School Canopy`** | Data from the Tree Canopy Equity Study, including the `school_canopy_data.csv`. |
| **`/Data/Watershed`** | Hydrologic layers: Groundwater basins, hydrogeologic forebays, and SCWP Watershed areas. |
| **`/Documentation`** | Metadata and Michael’s specific layer documentation (`Data Sources (Michael's layers)`). |
| **`/Figures`** | Analytical notebooks (`Plots_For_Project.ipynb`) and static exports like `Environmental Burden Distribution`. |
| **`/Requirements`** | Environment configuration and software dependency lists. |

---

## Methodology & Technical Stack
The core of this project is a Python-based data pipeline that performs spatial joins and applies a **Random Forest scoring algorithm** to identify priority sites.

### Technical Requirements
* **Language**: Python 3.8+
* **Geospatial**: `geopandas`, `shapely`, `fiona`
* **Analysis**: `pandas`, `numpy`, `scikit-learn`
* **Visualization**: `matplotlib`, `seaborn`



---

## Execution & Reproducibility
The analysis is designed to be fully reproducible and "cloud-ready." 

**No local data downloading is required** for the primary visualization suite. The code in `Figures/Plots_For_Project.ipynb` is configured to pull the latest data directly from this GitHub repository's `main` branch.

1.  **Clone the repo**: `git clone https://github.com/nouhy01/CWH-UCLA-Project.git`
2.  **Install dependencies**: `pip install -r Requirements/Software_Dependencies.txt`
3.  **Run Analysis**: Open `Plots_For_Project.ipynb` to regenerate the Environmental Burden and Poverty vs. Impact plots.

---

## Expected Outputs
The project generates several key metrics for decision-makers:
* **Heat Vulnerability Index**: Schools with the lowest canopy-to-student ratio.
* **Stormwater Capture Ranking**: Campuses sitting on "high-infiltration" soil types (Forebays).
* **Cumulative Impact Scores**: Schools in the top 10% of CalEnviroScreen burden.

---

## Acknowledgments
* **Nouh J. Sepulveda** – UCLA Undergraduate
* **Michael Adams Jr.** – UCLA Undergraduate
* **Professor Isabella arzno-soltero** – UCLA Civil & Environmental Engineering
* **Council for Watershed Health (CWH)**

---
