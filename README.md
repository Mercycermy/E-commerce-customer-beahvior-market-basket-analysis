# E-commerce Customer Behavior & Market Basket Analysis

## Project Overview

This repository analyzes e-commerce customer behavior and shopping patterns using a transaction-style dataset.

The workflow focuses on:
- Cleaning and preparing raw customer/order data
- Exploring behavioral patterns through visualization
- Summarizing actionable findings in a final report notebook

## Repository Structure

```text
E-commerce-customer-beahvior-market-basket-analysis/
├── data/
│   └── raw/
│       └── ecommerce_customer_data_custom_ratios.csv
├── notebooks/
│   ├── 01_cleaning.ipynb
│   ├── 03visual.ipynb
│   ├── 04_final_report.ipynb
│   └── data/
│       └── cleaned/
│           └── ecommerce_customer_data_cleaned.csv
├── requirements.txt
└── README.md
```

## Notebooks

- `notebooks/01_cleaning.ipynb`  
  Cleans and prepares the raw dataset for analysis.

- `notebooks/03visual.ipynb`  
  Performs exploratory analysis and visualizations of customer behavior and basket patterns.

- `notebooks/04_final_report.ipynb`  
  Consolidates insights, observations, and conclusions.

## Data Files

- Raw input: `data/raw/ecommerce_customer_data_custom_ratios.csv`
- Cleaned output: `notebooks/data/cleaned/ecommerce_customer_data_cleaned.csv`

## Tech Stack

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- mlxtend

## Setup

1. Clone this repository.
2. Create and activate a Python environment (recommended).
3. Install dependencies from `requirements.txt`.
4. Launch Jupyter and run notebooks in order.

## Typical Workflow

1. Run `01_cleaning.ipynb` to generate cleaned data.
2. Run `03visual.ipynb` for visual exploration.
3. Run `04_final_report.ipynb` for the final summary.

## Notes

- The folder name contains a typo (`beahvior`) and is kept as-is to match the existing repository name.
- If notebook paths differ on your machine, update relative paths inside notebook cells accordingly.

## Author

Maintained by the repository owner.
