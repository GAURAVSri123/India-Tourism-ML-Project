# 🇮🇳 India Tourism Machine Learning Project

### Forecasting Monthly Foreign Tourist Arrivals and Seasonal Clustering of Source Countries in India

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-K--Means-orange)
![Forecasting](https://img.shields.io/badge/Time%20Series-Forecasting-green)
![Status](https://img.shields.io/badge/Status-Project%20Completed-success)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter)

## 📌 Project Overview

Tourism plays an important role in India's economic development, contributing to employment, foreign exchange earnings, and cultural exchange.

This project applies **Machine Learning and Time Series Analysis** to Indian tourism statistics to understand historical tourism patterns, identify seasonal trends, group source countries based on their seasonal behaviour, and forecast future Foreign Tourist Arrivals (FTAs).

The project is divided into two major components:

- **Time Series Forecasting:** Analysing and forecasting monthly Foreign Tourist Arrivals in India.
- **Seasonal Clustering:** Applying K-Means clustering to group source countries based on their quarterly tourist arrival distribution.

The analysis uses official Indian tourism statistics.

## 🎯 Project Objectives

1. Analyse historical monthly Foreign Tourist Arrivals in India.
2. Identify tourism growth, decline, trends, and seasonal patterns.
3. Examine the impact of unusual events on international tourism.
4. Forecast future monthly Foreign Tourist Arrivals using time series techniques.
5. Identify similarities in seasonal tourism patterns across source countries.
6. Apply K-Means clustering to segment countries according to their quarterly arrival distributions.
7. Generate meaningful insights that can support tourism planning and decision-making.

## 📂 Datasets

The project uses two datasets derived from official tourism publications.

### 1. Monthly Foreign Tourist Arrivals Dataset

**File:** `India_Monthly_FTA_2019_2024.csv`

| Attribute | Description |
|---|---|
| Time period | January 2019 – December 2024 |
| Frequency | Monthly |
| Total observations | 72 |
| Target variable | Foreign Tourist Arrivals |
| Source | India Tourism Data Compendium 2025 |
| Reference | Table 2.2.1 |
| Original authority | Bureau of Immigration |

This dataset is used for exploratory data analysis, trend analysis, seasonality analysis, and forecasting.

### 2. Country-wise Tourism Dataset

**File:** `India_Tourism_Statistics_2024_Table_2.2.6(1).csv`

| Attribute | Description |
|---|---|
| Countries/territories | 209 |
| Features | 7 |
| Data type | Country-wise tourism statistics |
| Seasonal information | Quarterly distribution (Q1–Q4) |
| Source | India Tourism Statistics 2024 |

This dataset is used to identify similarities between source countries based on their quarterly tourism arrival patterns.

**Note:** Complete monthly country-wise observations were not available for the required period. Therefore, quarterly seasonal clustering was selected as the alternative approach.

## 🛠️ Technologies and Libraries

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Jupyter Notebook | Development and experimentation |
| Pandas | Data manipulation |
| NumPy | Numerical computations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine Learning and K-Means |
| Statsmodels | Statistical and time series analysis |
| SciPy | Statistical analysis |

## 📊 Project Methodology

### Part 1: Monthly Foreign Tourist Arrivals Forecasting

**Step 1 – Data Collection**

Collected official monthly Foreign Tourist Arrivals data covering 2019–2024.

**Step 2 – Data Preprocessing**

- Loaded the CSV dataset.
- Converted date columns into datetime format.
- Checked missing values and duplicate observations.
- Verified monthly frequency.
- Prepared the time series for analysis.

**Step 3 – Exploratory Data Analysis (EDA)**

Performed analysis to understand:

- Annual changes in foreign tourist arrivals.
- Monthly arrival distribution.
- Long-term tourism trends.
- Seasonal variations.
- Changes during and after the COVID-19 period.

**Step 4 – Seasonality and Trend Analysis**

Examined monthly and yearly tourism patterns to understand recurring seasonal behaviour and tourism recovery.

**Step 5 – Time Series Forecasting**

Applied time series forecasting techniques to model historical tourism behaviour and estimate future Foreign Tourist Arrivals.

**Step 6 – Model Evaluation**

Evaluated forecasting performance using suitable forecasting error metrics and compared model predictions.

### Part 2: Seasonal Clustering of Source Countries

**Step 1 – Data Preparation**

Prepared country-wise tourism data and extracted quarterly seasonal distribution features.

**Step 2 – Feature Engineering**

Selected quarterly features (Q1, Q2, Q3, Q4) to represent each country's seasonal tourism distribution.

**Step 3 – Data Standardization**

Applied StandardScaler to standardize numerical features.

**Step 4 – Log Transformation**

Applied log transformation to tourism arrival values to reduce the influence of large differences in country-wise arrival volumes.

**Step 5 – Selecting Optimal Clusters**

Evaluated different cluster configurations using the Silhouette Score.

**Step 6 – K-Means Clustering**

Applied the K-Means algorithm to group countries with similar tourism patterns.

**Step 7 – Cluster Interpretation**

Analysed cluster characteristics to understand differences in seasonal tourism behaviour among source countries.

## 📈 Key Preliminary Findings

### Monthly Tourism Analysis

- The dataset contains 72 monthly observations covering January 2019 to December 2024.
- Tourism arrivals experienced a substantial decline during the COVID-19 period.
- Tourism arrivals subsequently showed a recovery trend.
- January showed the highest normalized seasonal index (159.44).
- May showed the lowest normalized seasonal index (53.45).

### Annual Tourism Recovery

| Year | Average Monthly Arrivals |
|---|---:|
| 2019 | 910,862.92 |
| 2020 | 228,730.50 |
| 2021 | 127,259.50 |
| 2022 | 536,455.58 |
| 2023 | 793,410.67 |
| 2024 | 829,310.17 |

### Clustering Analysis

- K-Means was selected for country segmentation.
- The Silhouette Score for K=2 was 0.7175.
- The Silhouette Score for K=3 was 0.7001.
- K=2 was selected based on the comparison of these scores.

These results indicate meaningful differences in seasonal tourism patterns among source countries.

## 📁 Project Structure

```text
India-Tourism-ML-Project/
│
├── India_tourism ML project.ipynb
│
├── datasets/
│   ├── India_Monthly_FTA_2019_2024.csv
│   └── India_Tourism_Statistics_2024_Table_2.2.6(1).csv
│
├── results/
│   └── Tourism_Project_Results.xlsx
│
├── figures/
│
├── report/
│
└── README.md
```

*The directory structure represents the intended organization of the project files.*

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/GAURAVSri123/India-Tourism-ML-Project.git
```

### 2. Navigate to the Project Directory

```bash
cd India-Tourism-ML-Project
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

### 4. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels scipy jupyter openpyxl
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `India_tourism ML project.ipynb` and execute the notebook cells sequentially.

## 💡 Applications of the Project

The project can help:

- Understand international tourism demand in India.
- Identify seasonal tourism patterns.
- Forecast future tourist arrivals.
- Segment source countries according to seasonal behaviour.
- Support tourism planning and resource allocation.
- Assist tourism authorities in understanding international visitor trends.

## 🚀 Future Scope

Potential improvements include:

- Incorporating additional historical tourism observations.
- Comparing advanced forecasting models.
- Exploring external factors such as exchange rates, economic indicators, and international events.
- Developing interactive tourism dashboards.
- Performing more detailed country-level seasonal analysis.
- Updating the forecasting system with newly published tourism statistics.

## 📚 Data Sources

1. Ministry of Tourism, Government of India – [Official Website](https://tourism.gov.in/)
2. India Tourism Data Compendium 2025.
3. India Tourism Statistics 2024.
4. Bureau of Immigration, Government of India.

## 👨‍💻 Project Information

**Project Title:** Forecasting Monthly Foreign Tourist Arrivals and Seasonal Clustering of Source Countries in India

**Problem Number:** 73

**Domain:** Machine Learning and Tourism Analytics

**Development Environment:** Python and Jupyter Notebook

**Project Type:** Academic / Machine Learning Project

---

⭐ If you find this project useful, consider giving the repository a star!

**Made with Python, Machine Learning, and Data Analytics.**
