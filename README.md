# 🌲 HeatMappers Forest Modeling Project

This repository contains our team's work across **Sprints 1–4** for the forest modeling and classification challenge. The goal of this project is to develop machine learning models that predict key forest attributes — such as **DBH (Diameter at Breast Height), CBH (Crown Base Height), species, genus, and plant functional type (PFT)** — using a combination of **Aerial LiDAR (ALS)**, **Terrestrial LiDAR (TLS)**, and **imputed treelists from FastFuels**.

---

## 📊 Datasets Used

### External Datasets
- **FIA Database**: `CA_TREE.csv`, `CA_PLOT.csv`, `REF_SPECIES.csv`  
- **Field Survey Data**: `03_tree.csv`, `01_plot_identification.csv`  
- **ALS/TLS LiDAR Data**: USGS `.laz` files and `.ptx` TLS files  
- **FastFuels TreeMap 2016**: Treelists generated using the FastFuels API  
- **Geo Boundaries**: `independence_lake_boundary.geojson`, `sedgwick_boundary.geojson`  

### Derived Datasets
- `ttops.csv`: ALS-derived tree tops detected from CHM and peak detection  
- `tls_treelist.csv`: TLS-derived tree-level data  
- `fftl_plots.csv`: Predicted treelist from FastFuels for target plots  
- `combined_intelimon_metrics.csv`: TLS-derived structural metrics from IntELiMon  

---

## 🔧 Required Libraries

To run the notebooks, make sure you have the following Python libraries installed:

- numpy  
- pandas  
- matplotlib  
- seaborn  
- scikit-learn  
- xgboost *(optional for Sprint 1b)*  
- imblearn *(for SMOTE, optional)*  
- geopandas  
- rasterio  
- laspy  
- pyproj  
- folium  
- plotly  
- pdal  
- skimage  

We recommend using a virtual environment. You can install everything with:

```
pip install -r requirements.txt
```

Or using Conda:

```
conda create -n forest-modeling python=3.11  
conda activate forest-modeling  
pip install -r requirements.txt
```

---

## ▶️ Running Instructions

Follow these steps to run the project successfully:

1. **Clone the repository**  
   Open a terminal and run:  
   `https://github.com/Anshu-b/HeatMappers`  

2. **Install dependencies**  
   ```
   pip install -r requirements.txt
   ```

3. **Start Jupyter**  
   Run either:  
   `jupyter notebook`  
   or  
   `jupyter lab`

4. **Open and run the notebooks**  
   - Notebooks are organized by sprint (see below).  
   - Run all cells from top to bottom.  
   - Ensure data files are placed in `data/` or `inputs/` folders as needed.  
   - Outputs include classification reports, graphs, CHMs, and CSV files.

---

## 🗂️ Notebooks with our code by Sprint


### Sprint 1

`In order to run sprint 1a make sure unzip data.zip`

- `sprint1_1-4_heatmappers.ipynb` – Tasks 1–4 results  
- `sprint1_5-6_HeatMappers.ipynb` – ALS/TLS visualization + classification

### Sprint 2
- `sprint2_1-2_HeatMappers.ipynb` – CHM generation, ITD peak detection  
- `sprint2_3-4_HeatMappers.ipynb` – FastFuels API modeling

### Sprint 3

`In order to run sprint 3 make sure unzip data.zip`

- `sprint3_HeatMappers.ipynb` – TLS and field DBH comparison + modeling

### Sprint 4

`In order to run sprint 4 make sure unzip data.zip`

- `sprint4-1-field_HeatMappers.ipynb` – PFT, genus, and species classification from field data  
- `sprint4-2-tls-enhancement_HeatMappers.ipynb` – Predicting CBH and CR  
- `sprint4-3-ff_HeatMappers.ipynb` – Classification using FastFuels + predicted features  

---

## 📦 Expected Outputs

- Visualizations: CHMs, confusion matrices, histograms, treelist charts  
- Model metrics: Accuracy, F1-score, precision, recall  
- Classification reports per model/task  
- CSV outputs like `ttops.csv`, `fftl_plots.csv`  
- Final report summarizing all results and findings

---

## 📄 Final Report

Please see `HeatMappers_project_report.pdf` for:

- Model comparison (Random Forest, Logistic Regression, AdaBoost)  
- PFT, genus, and species prediction performance  
- Accuracy analysis of field-based vs. FastFuels-based models  
- Discussion and recommendations

---

## 👥 Team

**Team Name**: HeatMappers  
**Members**: 

- Ansh Bhatnagar
- Jiahe Qin
- Jeronimo Adames-Baena
- Ishayu Ghosh

---

## 📬 Submission Notes

- All notebooks for Sprints 1–4 are included in this repository.  
- Final report is submitted as: `HeatMappers_project_report.pdf`  
- URL to this repository is included in the Sprint 4 text submission.
