# Spark Funds Investment Analysis

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

An end-to-end exploratory data analysis project using Crunchbase startup investment data to identify the optimal funding type, investment-friendly English-speaking countries, and high-growth business sectors for Spark Funds.

---

# Overview

Spark Funds is an asset management company looking to invest in startups worldwide. The company follows a simple investment philosophy:

> **Invest where other investors are investing.**

The objective of this project is to identify:

- The most suitable funding type
- The best English-speaking countries for investment
- The highest-performing business sectors

using historical investment data from Crunchbase.

---

# Business Problem

Spark Funds has two investment constraints:

- Invest **between USD 5 million and USD 15 million** per funding round.
- Invest only in **English-speaking countries** for ease of communication.

Based on historical funding data, this project recommends the optimal investment strategy by analyzing funding patterns, country-level investments, and sector performance.

---

# Dataset

The analysis uses three datasets provided as part of the assignment.

| Dataset | Description |
|---------|-------------|
| **companies.csv** | Company information including country and business category |
| **rounds2.csv** | Startup funding round information |
| **mapping.csv** | Maps company categories into eight main business sectors |

---

# Project Workflow

```text
                   Crunchbase Data
                          │
                          ▼
                  Data Cleaning
                          │
                          ▼
             Merge Companies & Funding Data
                          │
                          ▼
               Funding Type Analysis
                          │
                          ▼
                 Country Analysis
                          │
                          ▼
                  Sector Mapping
                          │
                          ▼
            Sector-wise Investment Analysis
                          │
                          ▼
                 Data Visualization
                          │
                          ▼
            Investment Recommendations
```

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

# Analysis Methodology

The project was completed in six stages.

### 1. Data Cleaning

- Loaded investment and company datasets
- Standardized company identifiers
- Resolved encoding inconsistencies
- Merged datasets into a master dataframe
- Removed unnecessary columns
- Handled missing values

---

### 2. Funding Type Analysis

Compared four funding types:

- Venture
- Angel
- Seed
- Private Equity

Calculated the representative investment amount for each funding type and selected the funding type satisfying Spark Funds' preferred investment range.

---

### 3. Country Analysis

- Ranked countries based on total venture investment
- Selected the top English-speaking countries
- Filtered the dataset for further analysis

---

### 4. Sector Analysis

- Extracted the primary company category
- Mapped categories into eight business sectors
- Analyzed sector-wise investment trends
- Identified the most active sectors in each country

---

### 5. Investment Recommendation

Generated investment recommendations based on

- Funding amount
- Country
- Sector popularity

---

### 6. Data Visualization

Created visualizations showing

- Funding type comparison
- Country-wise investments
- Sector-wise investments

---

# Results

## Key Findings

| Category | Recommendation |
|----------|----------------|
| **Funding Type** | Venture |
| **Investment Range** | USD 5–15 Million |
| **Top Country** | United States |
| **Second Country** | United Kingdom |
| **Third Country** | India |
| **Top Sector** | Others |
| **Second Sector** | Social, Finance, Analytics & Advertising |
| **Third Sector** | News, Search & Messaging |

---

# Funding Type Analysis

The average investment amount was calculated for the four major funding types.

The analysis showed that **Venture Funding** falls within Spark Funds' preferred investment range of **USD 5–15 million**, making it the recommended investment type.

![Funding Type Analysis](reports/figures/funding_type_analysis.png)

---

# Country Analysis

The top nine countries were ranked based on total venture investments.

Among English-speaking countries, the highest investment amounts were received by:

1. 🇺🇸 United States
2. 🇬🇧 United Kingdom
3. 🇮🇳 India

![Top Countries](reports/figures/top9_countries.png)

---

# Sector Analysis

Each company's primary business category was mapped into one of eight major sectors using the provided mapping dataset.

Sector-wise investment analysis identified the sectors receiving the highest number of investments in the top three countries.

The most active sectors were:

- Others
- Social, Finance, Analytics & Advertising
- News, Search & Messaging

![Sector Analysis](reports/figures/sector_analysis.png)

---

# Repository Structure

```text
Spark-Funds-Investment-Analysis/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── companies.csv
│   ├── rounds2.csv
│   └── mapping.csv
│
├── notebooks/
│   └── Spark_Funds_Investment_Analysis.ipynb
│
├── reports/
│   ├── Spark_Funds_Investment_Analysis_Presentation.pdf
│   ├── Investment_Analysis_Results.xlsx
│   └── figures/
│       ├── funding_type_analysis.png
│       ├── top9_countries.png
│       └── sector_analysis.png
│
└── src/
    └── helper_functions.py
```

---

# How to Run

Clone the repository:

```bash
git clone https://github.com/<your-username>/Spark-Funds-Investment-Analysis.git
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
notebooks/Spark_Funds_Investment_Analysis.ipynb
```

Run all cells to reproduce the analysis and figures.

---

# Future Improvements

- Interactive dashboards using Plotly or Tableau
- Automated data validation pipeline
- Investment trend forecasting using machine learning
- Interactive country and sector visualizations
- Cloud-based data pipeline for large-scale investment analysis

---

# Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Wrangling
- Data Visualization
- Business Intelligence
- Investment Analytics
- Sector Mapping
- Feature Engineering
- Python Programming
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

# Author

**Hanaa Parvez Khan**

PG Diploma in Machine Learning and AI

GitHub: https://github.com/<your-username>

---

## License

This project is licensed under the **MIT License**.

> **Note:** The datasets used in this project were provided as part of an academic assignment based on Crunchbase data. Before making the repository public, ensure that sharing the raw datasets complies with the course requirements and the applicable data licensing terms.
