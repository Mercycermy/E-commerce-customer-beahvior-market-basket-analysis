# E-commerce Customer Data Cleaning Project

This project focuses on cleaning and validating e-commerce customer transaction data for downstream analysis.

## Dataset Overview

The dataset contains customer transaction records with the following key information:
- **Customer Details**: ID, Name, Age, Gender
- **Transaction Data**: Purchase Date, Product Category, Price, Quantity, Total Amount
- **Payment Info**: Payment Method, Returns, Churn Status

## Current Project Structure

```text
ecommerce-data-cleaning/
├── data/
│   └── raw/
│       └── ecommerce_customer_data_custom_ratios.csv
├── notebooks/
│   ├── 01_cleaning.ipynb    # Data cleaning notebook
│   ├── 03visual.ipynb       # Data visualization notebook
│   └── data/
│       └── cleaned/
│           └── ecommerce_customer_data_cleaned.csv
├── requirements.txt
└── README.md
```

## Data Cleaning Process

### Step-by-Step Cleaning Workflow

1. **Data Loading & Exploration**
   - Load CSV data using pandas
   - Inspect data structure, types, and basic statistics
   - Identify columns and data patterns

2. **Missing Value Analysis**
   - Check for null values across all columns
   - Calculate missing value percentages
   - Visualize missing data patterns

3. **Handle Duplicate Columns**
   - Remove redundant 'Customer Age' column (duplicate of 'Age')
   - Streamline dataset structure

4. **Data Type Conversions**
   - Convert 'Purchase Date' to datetime format
   - Ensure numeric columns are properly typed
   - Handle conversion errors gracefully

5. **Missing Value Treatment**
   - Fill missing 'Returns' values with 0 (business assumption)
   - Document assumptions made during cleaning

6. **Data Consistency Checks**
   - Validate categorical values (Product Category, Payment Method, Gender)
   - Check for logical inconsistencies (negative prices, invalid ages)
   - Identify data entry errors

7. **Business Logic Validation**
   - Verify Total Purchase Amount = Product Price × Quantity
   - Flag inconsistent calculations for review

8. **Data Quality Fixes**
   - Correct obvious gender mismatches (e.g., "Christine" marked as "Male")
   - Standardize categorical values

9. **Outlier Detection**
   - Use IQR method to identify outliers in price, quantity, and amounts
   - Visualize distributions with histograms and boxplots

10. **Final Validation & Export**
    - Generate data quality summary report
    - Export cleaned dataset for analysis

### Key Data Quality Issues Identified

- **Duplicate Columns**: 'Customer Age' and 'Age' contain identical data
- **Missing Values**: Some 'Returns' values are missing
- **Gender Inconsistencies**: Names don't match assigned genders in some records
- **Business Logic**: Need to verify calculation accuracy (Price × Quantity = Total)

## Getting Started

### Prerequisites
```bash
pip install -r requirements.txt
```

### Running the Cleaning Process
1. Open `notebooks/01_cleaning.ipynb`
2. Run cells sequentially following the 10-step process
3. Each step includes explanations and validation checks
4. Monitor output for data quality issues and corrections

### Expected Outputs
- Cleaned dataset with resolved data quality issues
- Data quality summary report
- Documentation of all cleaning decisions made

## Visualizations & Insights

The `notebooks/03visual.ipynb` notebook explores the cleaned dataset to uncover key business insights regarding:
- **Demographics**: Understanding the active customer base through age and gender distributions.
- **Revenue Drivers**: Identifying high-value product categories by analyzing total revenue and purchase amounts.
- **Customer Retention & Returns**: Exploring customer churn rate and the percentage of returned products across different categories to inform retention strategies.

To view the charts and analysis, run the notebook sequentially.

## Data Dictionary

| Column | Description | Data Type | Notes |
|--------|-------------|-----------|-------|
| Customer ID | Unique customer identifier | Integer | Primary key |
| Purchase Date | Transaction timestamp | Datetime | Format: YYYY-MM-DD HH:MM:SS |
| Product Category | Product classification | String | Electronics, Home, Clothing, Books |
| Product Price | Unit price of product | Float | In currency units |
| Quantity | Number of items purchased | Integer | Must be positive |
| Total Purchase Amount | Total transaction value | Float | Should equal Price × Quantity |
| Payment Method | Payment type used | String | Credit Card, PayPal, Cash |
| Age | Customer age in years | Integer | Cleaned duplicate of Customer Age |
| Returns | Return indicator | Float | 0.0 = No return, 1.0 = Returned |
| Customer Name | Customer full name | String | Used for gender validation |
| Gender | Customer gender | String | Male, Female |
| Churn | Customer churn indicator | Integer | 0 = Active, 1 = Churned |

## Notes
- This is a focused data cleaning project - analysis notebooks have been removed
- Run notebook cells manually to maintain control over the cleaning process
- All cleaning steps include detailed explanations and business logic validation
