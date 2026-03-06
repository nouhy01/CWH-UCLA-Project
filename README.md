# CWH-UCLA-Project: School Greening & Watershed Equity
### Identifying Intersectional Opportunity Sites for Stormwater & Equity

[![UCLA Engineering](https://img.shields.io/badge/UCLA-Civil%20%26%20Environmental-blue)](https://samueli.ucla.edu/)
[![Partner](https://img.shields.io/badge/Partner-Council%20for%20Watershed%20Health-green)](https://www.watershedhealth.org/)

---

### 🔗 [Access the Live Dashboard Here](https://cwh-dashboard.surge.sh/)

## Project Overview
[cite_start]Public schools in Los Angeles County often lack adequate tree canopy, contributing to "Urban Heat Island" effects that disproportionately impact disadvantaged communities[cite: 9, 10]. [cite_start]Simultaneously, LA’s watershed requires more permeable surfaces for stormwater capture[cite: 14, 26]. 

[cite_start]This project solves the "Data Fragmentation" problem by merging environmental, hydrological, and socioeconomic datasets into a **Unified School Layer**[cite: 11, 12, 13, 14]. [cite_start]This tool allows partners to prioritize greening projects where they provide the most significant community and environmental ROI[cite: 5, 6, 7].

## Technical Refinements & Methodology
Following the ENHANCE phase, the analysis was improved through:
* **Discrepancy Analysis**: Included a 95% confidence interval to statistically confirm that current high-priority areas often lack adequate permeability.
* **Regional Burden Profiles**: Implemented Windrose Charts to visualize how stressors like heat and pollution interact across LAUSD regions.
* **Data Validation**: Corrected unit measurements (converted Square Inches to Square Meters) and applied logarithmic scaling to canopy percentage to better distinguish high-priority sites.
* **Visual Transparency**: Implemented a high-contrast color scheme: Schools (Red), Parks (Blue), and Overlap (Purple).

## How to Use the Dashboard
[cite_start]The **CWH School Greening Priority Dashboard** is an interactive web map designed for non-technical users to make data-driven decisions[cite: 18, 19]:

1. [cite_start]**Explore the Map**: Redder colors indicate higher priority[cite: 33]. Use the school counter to see both the total count and the schools visible in your current view.
2. [cite_start]**Adjust the Weights**: Use the **Scoring** tab to customize the index[cite: 22]. Per the March 2nd meeting, the default weights are:
    * [cite_start]**30%** Canopy Heat Relief [cite: 23]
    * [cite_start]**25%** Infiltration Potential [cite: 28]
    * [cite_start]**25%** Disadvantaged Community (CalEnviroScreen 5.0) [cite: 25]
    * **10%** Parks within 1/2 mile
    * **5%** Parks within 1/4 mile
    * **5%** Elementary School Status
3. [cite_start]**Check the Leaderboard**: The **Statistics** tab provides a "Top 20" list of schools meeting your specific criteria[cite: 29, 30].
4. [cite_start]**View Site Details**: Click any school to see its specific "Data Card," including enrollment and tree canopy percentage[cite: 33].

## Execution & Reproducibility
The analysis is designed to be fully reproducible using Python and Jupyter.

### Technical Requirements
* **Language**: Python 3.8+
* **Geospatial**: `geopandas`, `shapely`
* **Analysis**: `pandas`, `numpy`
* **Visualization**: `matplotlib`
* **ArcGIS Pro**

### Running Locally
1. **Clone the Repo**:
   ```bash
   git clone [https://github.com/nouhy01/CWH-UCLA-Project.git](https://github.com/nouhy01/CWH-UCLA-Project.git)
   
## Data Dictionary & Repository Structure
Files for ArcGIS layers can be downloaded here:
[Google Drive Link](https://drive.google.com/file/d/1Z6dWAoYiOX90I0CmPKkzbGt18-a-DBjL/view?usp=sharing)

```text
CWH-UCLA-Project/
├── Data/
│   ├── Community Characteristics/   # Socioeconomic datasets, Tree Equity, CES 5.0
│   ├── SCWP Layer/                  # Safe, Clean Water Program Opportunity spatial data
│   ├── Schools/                     # Points/polygons for schools and parks mapping
│   └── Watershed/                   # Hydrologic spatial layers (Basins, GDBs)
├── Figures/                         # Generates visualizations and analytical suites
│   ├── Plots_For_Project.ipynb      # Main Jupyter notebook for data analysis
│   └── [Exported Visuals]           # PNGs/PDFs of output charts
├── Requirements/                    # Environment setup files
│   └── Software_Dependencies.txt    # Python package dependencies
└── README.md                        # Project documentation

## Acknowledgments
* **Nouh J. Sepulveda** – UCLA Undergraduate
* **Michael Adams Jr.** – UCLA Undergraduate
* **Professor Isabella Arzeno-Soltero** – UCLA Civil & Environmental Engineering
* **Council for Watershed Health (CWH)**

---
