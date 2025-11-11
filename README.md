# Tire Wear and Lifespan Analysis

This project analyzes real-world tire usage data to understand factors affecting tire wear and overall lifespan. It demonstrates data cleaning, exploratory data analysis, and preparation of a structured dataset suitable for further statistical modeling or reporting. This work simulates practical tasks aligned with a forensic tire analysis and R&D environment.

---

## Objectives
- Collect or generate a dataset of 1,000+ tire records.
- Explore and validate data using Python (pandas).
- Identify and address missing values, outliers, and formatting issues.
- Produce a clean and analyzable dataset.
- Summarize observed patterns related to tire wear and replacement.

---

## Dataset Description

| Column | Description |
|--------|-------------|
| tire_id | Unique identifier for each tire |
| vehicle_type | Category of vehicle (e.g., car, truck, van) |
| mileage_km | Vehicle mileage at measurement time |
| tire_age_months | Tire age in months |
| initial_tread_mm | Original tread depth |
| current_tread_mm | Measured tread depth |
| wear_mm | Calculated wear (initial - current) |
| tire_pressure_psi | Tire inflation pressure |
| load_index | Load capacity rating |
| speed_rating | Speed performance class |
| ambient_temp_c | Temperature during usage |
| replacement_flag | 1 = needs replacement, 0 = usable |

---

## Methodology

### 1. Data Loading
- Loaded dataset using pandas.
- Inspected structure with `.head()`, `.info()`, `.describe()`.

### 2. Data Cleaning
- Removed exact duplicates.
- Identified missing values and imputed:
  - Numerical columns → median
  - Categorical columns → mode
- Checked for inconsistent ranges (e.g., tread depth cannot be negative).
- Recomputed `wear_mm` and `replacement_flag` for consistency.

### 3. Outlier Detection
- Used Interquartile Range (IQR) method to detect extreme outliers.
- Applied percentile capping (1st–99th percentile) to reduce skew.

### 4. Exploratory Analysis
- Visualized distributions (histograms, boxplots).
- Examined mileage vs. wear trends through scatterplots.
- Calculated correlations between wear and measured variables.

---

## Key Insights
- Higher mileage generally corresponds with greater tread wear.
- Tires with consistently lower pressure show faster wear progression.
- Tire aging (in months) contributes to wear, independent of mileage.
- Environmental temperature variations show moderate influence on wear patterns.

---

## Tools Used
- Python (pandas, numpy)
- matplotlib / seaborn
- Jupyter Notebook

---

## Repository Structure
