# 🌲 HeatMappers Forest Modeling Project

This repository contains our team's work across Sprints 1–4 for the forest modeling and classification challenge. The goal of this project is to develop machine learning models that predict important forest attributes (e.g., DBH, CBH, species, genus, plant functional type) from aerial and terrestrial LiDAR data, as well as imputed statistical treelists.


---

## 📊 Datasets Used

### External Sources:
- **FIA Database**: CA_TREE.csv, CA_PLOT.csv, REF_SPECIES.csv  
- **Field Survey Data**: 03_tree.csv, 01_plot_identification.csv  
- **ALS/TLS LiDAR Data**: USGS .laz files, PTX TLS files  
- **FastFuels TreeMap 2016**: Treelists generated using FastFuels API  
- **Boundaries**: independence_lake_boundary.geojson, sedgwick_boundary.geojson  

### Derived Datasets:
- `ttops.csv` — Tree tops detected from ALS via CHM + ITD  
- `tls_treelist.csv` — TLS-derived tree lists  
- `fftl_plots.csv` — FastFuels population treelist  
- `combined_intelimon_metrics.csv` — TLS structural metrics from IntELiMon  

---

## 🔧 Required Libraries

The following libraries are needed to run the notebooks successfully:

```bash
# Core
numpy
pandas
matplotlib
scikit-learn
seaborn

# Spatial and LiDAR
geopandas
rasterio
laspy
pyproj
folium
plotly
pdal
skimage

# ML utilities
xgboost (optional for Sprint 1b)
imblearn (for SMOTE in classification)



