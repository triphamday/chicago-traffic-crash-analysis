# 🚧 Chicago Traffic Crash Analysis (2022–2024)

### Project Overview

This project analyzes traffic crash data in Chicago from Jan 2022 to Oct 2024. It explores crash patterns and builds a machine learning model to predict crash severity. Tools used: Python (EDA, modeling), Power BI (visualization).

### Project Structure
```bash
.
├── PowerBI/
│   └── visualize.pdf               # Power BI dashboards and analysis
├── analysis/
│   ├── crashes-analysis.ipynb     # Deep-dive into crash trends
│   ├── overall-analysis.ipynb     # Summary-level insights
│   └── people-vehicles-analysis.ipynb # Analysis involving people and vehicles
├── model/
│   └── model-crashes.ipynb        # Modeling crash severity
├── pre_processing_and_eda/
│   ├── 1.initial-pre-processing.ipynb
│   ├── 2.data_overview.ipynb
│   └── 3.data-cleaning.ipynb
├── README.md                      # Project documentation
├── report.pdf                     # Full project report
└── slide.pdf                      # Summary presentation
```
### Data Preprocessing and EDA

- Filter date range (01/2022 – 10/2024)
- Remove columns with >60% nulls, fix types, drop duplicates
- Visualize and impute missing values (KNN, default values)
- Drop irrelevant/uniform columns
- Outlier handling on age, location

### Analysis by PowerBI

- **Time Trends**: Peak in May; risky hours 6–9 AM, 3–6 PM  
- **Vehicle & Behavior**: Camry, Corolla, Civic top crash vehicles; common risks: evading police, phone use  
- **Injury & Damage**: Severe damage in angle/rear-end crashes; most >$1,500  
- **Geography**: Hotspots downtown & near Lake Michigan; high fatalities in North Lawndale & Stickney

### Modeling

- **Target**: `most_severe_injury` (5 classes)
- **Features**: Selected via IV, WoE, ANOVA
- **Models**: RF, LightGBM, XGBoost, CatBoost, SGD
- **Top Accuracy**: LightGBM & XGBoost (~93.47%)

### How to Run
1. Clone the repository:
```bash
git clone <repository-url>
cd chicago-crash-analysis
```
2. Install required packages:
```bash
pip install -r requirements.txt
```
3.Run notebooks in this order:
- pre_processing_and_eda/
- analysis/
- model/

4. View visualizations in PowerBI/visualize.pdf

### Acknowledgments

- Open Data Portal by [City of Chicago](https://data.cityofchicago.org)  
- Project for course: **Data Analysis and Visualization (DS105) – UIT**

