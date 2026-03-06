# CWH-UCLA-Project: School Greening & Watershed Equity
### Identifying Intersectional Opportunity Sites for Stormwater & Equity

[![UCLA Engineering](https://img.shields.io/badge/UCLA-Civil%20%26%20Environmental-blue)](https://samueli.ucla.edu/)
[![Partner](https://img.shields.io/badge/Partner-Council%20for%20Watershed%20Health-green)](https://www.watershedhealth.org/)

---

### [Access the Live Dashboard Here](https://cwh-dashboard.surge.sh/)

## Project Overview
Public schools in Los Angeles County often lack adequate tree canopy, contributing to "Urban Heat Island" effects that disproportionately impact disadvantaged communities. Simultaneously, LA’s watershed requires more permeable surfaces for stormwater capture. 

This project solves the "Data Fragmentation" problem by merging environmental, hydrological, and socioeconomic datasets into a **Unified School Layer**. This tool allows partners to prioritize greening projects where they provide the most significant community and environmental ROI.

## How to Use the Dashboard
The **CWH School Greening Priority Dashboard** is designed for non-technical users to make data-driven decisions:

1. **Explore the Map**: Each dot represents a K-12 campus. Redder colors indicate higher priority based on the current scoring.
2. **Adjust the Weights**: Use the **Scoring** tab to change how much you value different factors like **Canopy Heat Relief**, **Infiltration Potential**, or **Disadvantaged Communities**.
3. **Check the Leaderboard**: The **Statistics** tab provides a "Top 20" list of schools that meet your specific criteria.
4. **View Site Details**: Click any school to see its specific "Data Card," including enrollment, current canopy percentage, and local soil types.

## Step-by-Step Instructions for Reproducibility

### Option 1: The Easiest Way (No Coding Required)
If you want to view the analysis and charts without installing software, use **Google Colab**:
1. Go to [Google Colab](https://colab.research.google.com/).
2. Select the **GitHub** tab.
3. Enter the URL: `https://github.com/nouhy01/CWH-UCLA-Project`
4. Open `Figures/Plots_For_Project.ipynb` and click **Runtime > Run All**.

### Option 2: Running Locally (For Technical Users)
1. **Clone the Repo**: `git clone https://github.com/nouhy01/CWH-UCLA-Project.git`
2. **Install Dependencies**: `pip install -r Requirements/Software_Dependencies.txt`
3. **Run Analysis**: Open the `Plots_For_Project.ipynb` notebook in VS Code or Jupyter to regenerate all analytical charts.

---

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
