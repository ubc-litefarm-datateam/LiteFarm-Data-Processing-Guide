# LiteFarm-Data-Processing-Guide

This repository hosts the documentation and code for the **Farm Validation Project**. The primary goal of this project is to clean, validate, and preprocess farm-related data by identifying fake/invalid farms and removing outliers. By doing so, we aim to ensure the resulting data is interpretable and produces unskewed visualizations and results.

---

## Project Overview

In this project, we employ a combination of techniques to:
1. **Identify Fake or Invalid Farms**:
   - Validate farm attributes such as geographic location, shape, size, and names.
   - Detect inconsistencies in the data (e.g., incorrect email formats, duplicate entries).
   - Use geospatial data to determine if farms are located in feasible areas (e.g., land vs. ocean).

2. **Remove Outliers**:
   - Analyze farm data for outliers in terms of area, harvest yield, and other key metrics.
   - Implement robust statistical methods to detect and handle anomalies.
   - Focus on creating datasets that are free from extreme values, ensuring interpretable and unbiased visualizations.

---

## Key Features

### Documentation
All documentation is built using **Quarto** and includes:
- **Outlier Detection**:
  - [`farm_area_analysis.qmd`](docs/farm_area_analysis.qmd): Analysis of farm areas to detect invalid entries.
  - [`farm_centroid_validation.qmd`](docs/farm_centroid_validation.qmd): Validates whether farm centroids align with their expected locations.
- **Outlier Detection**:
  - [`outlier_detection.qmd`](docs/outlier_detection.qmd): Techniques to identify and handle data anomalies in key metrics such as area and yield.
- **Data Cleaning Techniques**:
  - [`filter_emails.qmd`](docs/filter_emails.qmd): Identifies and removes invalid email entries.
  - [`filter_farm_names.qmd`](docs/filter_farm_names.qmd): Standardizes and validates farm names.

### Geospatial Data Analysis
- Use of `.shp` files to validate farm locations and boundaries.
- Validation of whether farms are located on land or water using spatial mapping techniques.

### CI/CD Integration
- The documentation is automatically built and published using **GitHub Actions** and **GitHub Pages** for live updates.
- Hosted documentation URL: [Farm Validation Documentation](https://your-org.github.io/farm-validation-documentation)

---

## Setup Instructions

### Prerequisites
- [Quarto](https://quarto.org/)
- Python (with dependencies listed in `requirements.txt`)
- Geospatial libraries for handling `.shp` and `.shx` files (e.g., `geopandas`, `shapely`).


