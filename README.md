# CWH-UCLA-Project: School Greening & Watershed Equity
### Identifying Intersectional Opportunity Sites for Stormwater & Equity

[![UCLA Engineering](https://img.shields.io/badge/UCLA-Civil%20%26%20Environmental-blue)](https://samueli.ucla.edu/)
[![Partner](https://img.shields.io/badge/Partner-Council%20for%20Watershed%20Health-green)](https://www.watershedhealth.org/)

---

### 🔗 [Access the Live Dashboard Here](https://cwh-dashboard.surge.sh/)

---

## Project Overview

Public schools in Los Angeles County often lack adequate tree canopy, contributing to **Urban Heat Island** effects that disproportionately impact disadvantaged communities. Simultaneously, LA’s watershed requires more permeable surfaces for stormwater capture.

This project solves the **data fragmentation problem** by merging environmental, hydrological, and socioeconomic datasets into a **Unified School Layer**. This tool allows partners to prioritize greening projects where they provide the greatest community and environmental return on investment.

---

## Technical Refinements & Methodology

Following the **ENHANCE phase**, the analysis was improved through:

- **Discrepancy Analysis**  
  Included a **95% confidence interval** to statistically confirm that current high-priority areas often lack adequate permeability.

- **Regional Burden Profiles**  
  Implemented **Windrose Charts** to visualize how stressors like heat and pollution interact across LAUSD regions.

- **Data Validation**  
  Corrected unit measurements by converting **square inches to square meters** and applied **logarithmic scaling** to canopy percentage to better distinguish high-priority sites.

- **Visual Transparency**  
  Implemented a **high-contrast color scheme**:
  - Schools → **Red**
  - Parks → **Blue**
  - Overlap → **Purple**

---

## How to Use the Dashboard

The **CWH School Greening Priority Dashboard** is an interactive web map designed for non-technical users to make data-driven decisions.

### 1. Explore the Map
Redder colors indicate higher priority. Use the **school counter** to see both the total count and the schools visible in your current view.

### 2. Adjust the Weights
Use the **Scoring** tab to customize the index.

Default weights (from the March 2 meeting):

- **30%** Canopy Heat Relief  
- **25%** Infiltration Potential  
- **25%** Disadvantaged Community (CalEnviroScreen 5.0)  
- **10%** Parks within 1/2 mile  
- **5%** Parks within 1/4 mile  
- **5%** Elementary School Status  

### 3. Check the Leaderboard
The **Statistics** tab provides a **Top 20 list** of schools meeting your selected criteria.

### 4. View Site Details
Click any school to open its **Data Card**, which includes:

- Enrollment
- Tree canopy percentage
- Additional site metrics

---

## Execution & Reproducibility

The analysis is designed to be **fully reproducible using Python and Jupyter**.

### Technical Requirements

- **Language:** Python 3.8+
- **Geospatial:** `geopandas`, `shapely`
- **Analysis:** `pandas`, `numpy`
- **Visualization:** `matplotlib`
- **GIS Platform:** ArcGIS Pro

---

## Running Locally

### 1. Clone the Repository

```bash
git clone https://github.com/nouhy01/CWH-UCLA-Project.git
```

### 2. Install Dependencies

Ensure Python 3.8+ is installed, then run:

```bash
pip install -r Requirements/Software_Dependencies.txt
```

### 3. Run the Analysis

Open the notebook:

```
Figures/Plots_For_Project.ipynb
```

in **VS Code** or **Jupyter Notebook** to regenerate all charts and analytical figures.

---

## Data Dictionary & Repository Structure

Files for ArcGIS layers can be downloaded from the project **Google Drive repository**.

### Repository Structure

```
CWH-UCLA-Project/
├── Data/
│   ├── CSNA/                        # GeoJSON layers for community opportunity areas
│   ├── Closed Schools/              # Historical data for decommissioned campuses
│   ├── Community Characteristics/   # Socioeconomic datasets, Tree Equity, CES 5.0
│   ├── SCWP Layer/                  # Safe Clean Water Program opportunity spatial data
│   ├── Schools/                     # Points/polygons for schools and parks mapping
│   └── Watershed/                   # Hydrologic spatial layers (Basins, GDBs)
│
├── Figures/
│   ├── Plots_For_Project.ipynb      # Main Jupyter notebook for analysis
│   └── Exported Visuals/            # PNG or PDF charts generated from analysis
│
├── Requirements/
│   └── Software_Dependencies.txt    # Python dependency list
│
└── README.md                        # Project documentation
```

---

## Data Dictionary

| Folder / File | Description |
|---|---|
| `/Data/CSNA` | Community Strategy Needs Assessment spatial opportunity layers |
| `/Data/Closed Schools` | Historical datasets for decommissioned campuses |
| `/Data/Community Characteristics` | Socioeconomic indicators, Tree Equity, CalEnviroScreen 5.0 |
| `/Data/School Canopy` | Tree canopy equity study and urban heat island data |
| `/Data/Watershed` | Hydrologic layers including groundwater basins and watershed areas |
| `/Figures` | Analytical outputs and visualizations generated from the notebook |
| `/Requirements` | Python environment dependencies needed to reproduce the analysis |

---

## Acknowledgments

**Nouh J. Sepulveda** — UCLA Undergraduate  
**Michael Adams Jr.** — UCLA Undergraduate  

**Professor Isabella Arzeno-Soltero**  
UCLA Civil & Environmental Engineering  

**Council for Watershed Health (CWH)**
