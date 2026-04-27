# Gun Violence Analysis — EDA & Political Context

Exploratory analysis of gun violence incidents in the United States (2013–2018), enriched with state-level population, electoral polarization, and gun law data to examine patterns beyond raw incident counts.

## What this project does

- Loads and cleans ~240,000 gun violence incidents from the Gun Violence Archive
- Engineers features: date components, incident type flags (one-hot encoding), participant status
- Imputes missing coordinates using state-level averages
- Builds choropleth maps of incidents by state (absolute and per 100k population)
- Cross-references with 2016 election results to analyze the relationship between political polarization and gun violence rates
- Visualizes incident rates vs. electoral margin of victory, scaled by number of state gun laws

## Techniques used

- Exploratory Data Analysis (EDA)
- Feature engineering & one-hot encoding
- Geospatial visualization (choropleth maps — Plotly)
- Multi-dataset merging and normalization by population
- Interactive scatter plots with bubble sizing

## Stack

Python · Pandas · NumPy · Plotly · Seaborn · Matplotlib · Shapely · Scikit-learn · TensorFlow · Pathlib

## Datasets

This project uses 3 public datasets. **None are included in the repository** due to file size. Download and place them in a `data/` folder before running the notebook.

| File | Source | Notes |
|---|---|---|
| `gun-violence-data_01-2013_03-2018.csv` | [Kaggle — Gun Violence Data](https://www.kaggle.com/datasets/jameslko/gun-violence-data) | ~240k incidents, James Ko (2018) |
| `scprc-est2017-18+pop-res.csv` | [U.S. Census Bureau](https://www2.census.gov/programs-surveys/popest/datasets/2010-2017/state/asrh/scprc-est2017-18+pop-res.csv) | State population estimates 2017 |
| `federalelections2016.xlsx` | [MIT Election Data + Science Lab](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/42MVDX) | 2016 presidential results by state |

## How to run

```bash
git clone https://github.com/tu-usuario/gun-violence-analysis.git
cd gun-violence-analysis

# Create data folder and download datasets (see table above)
mkdir data

pip install -r requirements.txt
jupyter notebook gun_violence_analysis.ipynb
```

## Repository structure

```
gun-violence-analysis/
├── gun_violence_analysis.ipynb   # Full analysis
├── requirements.txt
├── data/
│   └── README.md                 # Download instructions for datasets
└── README.md
```

## Author

Dámaso López, Alexis Aminadab · Islas Zicatl, Max Emiliano · Mares Guerra, José de Jesús · Martínez Sánchez, José Ricardo · Salazar Argáez, Miguel Angel — Statistical Methods and Mathematics for Data Science Diploma