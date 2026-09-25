# Global Superstore EDA

Exploratory data analysis of the **Global Superstore** dataset to understand sales, profitability, customers, products, discounts, markets, regions, and shipping performance.

## Project Overview

This project uses Python-based exploratory data analysis to transform transactional retail data into business-focused insights.

The analysis covers:

- Data quality and cleaning
- Sales and profit KPIs
- Product and sub-category performance
- Regional and country-level analysis
- Market-level performance
- Customer analysis
- Discount and profitability analysis
- Shipping analysis
- Correlation analysis
- Year-over-year sales and profit trends

The objective is not only to visualize the data, but also to identify patterns that can support further business investigation.

## Key Metrics

| Metric | Result |
|---|---:|
| Total Sales | **$12.64M** |
| Total Profit | **$1.47M** |
| Orders | **25,035** |
| Customers | **4,873** |
| Overall Profit Margin | **11.61%** |
| Dataset Rows | **51,290** |

## Key Findings

### Product Performance

- **Technology** generated the highest total profit among the three product categories.
- **Phones** generated the highest sales among sub-categories.
- **Tables** was the only sub-category with negative total profit in the analysis.
- Loss-making products and sub-categories require further investigation of pricing, discounts, shipping costs, and product mix.

### Geographic Performance

- The **United States** generated the highest total sales and total profit among countries.
- **APAC** generated the highest aggregate sales and profit among the listed markets.
- Regional and country performance varies substantially, so sales should be evaluated together with profitability and margin.

### Discount & Profitability

- Higher discount levels are generally associated with lower aggregate profit in this dataset.
- The correlation between **Discount** and **Profit** is approximately **-0.316**.
- Several higher discount levels recorded negative aggregate profit.
- These results describe observed relationships in the dataset and **do not establish that discounts alone cause lower profit**.

### Customer Performance

- **Tom Ashbrook** generated the highest total sales among customers.
- **Tamara Chand** generated the highest total profit among customers.
- The highest-sales customer was not the highest-profit customer, demonstrating why customer analysis should consider both revenue and profitability.

### Time Trends

From 2011 to 2014, both total sales and total profit increased in the dataset:

| Year | Sales | Profit |
|---|---:|---:|
| 2011 | $2.26M | $248.94K |
| 2012 | $2.68M | $307.42K |
| 2013 | $3.41M | $406.94K |
| 2014 | $4.30M | $504.17K |

## Correlation Highlights

The numeric correlation analysis identified several notable relationships:

| Variables | Correlation |
|---|---:|
| Sales ↔ Shipping Cost | **0.768** |
| Sales ↔ Profit | **0.485** |
| Sales ↔ Quantity | **0.314** |
| Profit ↔ Discount | **-0.316** |

Correlation measures linear association; it does not establish causation.

## Data Quality & Preparation

The notebook performs several data-quality checks before analysis:

- Removed the redundant `记录数` / Number of Records column.
- Checked for missing values.
- Checked for duplicate rows.
- Converted date fields to datetime format.
- Examined numerical outliers using the IQR method.
- Retained identified outliers where they could represent legitimate business transactions rather than automatically deleting them.

## Analysis Workflow

```text
Raw Dataset
    │
    ├── Data Understanding
    ├── Data Quality Checks
    ├── Cleaning & Preparation
    ├── Outlier Analysis
    │
    ├── KPI Analysis
    ├── Product Analysis
    ├── Geographic Analysis
    ├── Customer Analysis
    ├── Discount Analysis
    ├── Shipping Analysis
    ├── Correlation Analysis
    └── Time & Market Trends
             │
             ▼
      Business Insights
```

## Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

## Repository Structure

```text
global-superstore-eda/
│
├── global-superstore-eda (1).ipynb
└── README.md
```

## Dataset

The notebook uses the **Global Superstore** transactional dataset and loads it from a Kaggle dataset path.

The notebook currently expects the dataset to be available at:

```text
/kaggle/input/datasets/fatihilhan/global-superstore-dataset/superstore.csv
```

Because the dataset is not stored in this repository, the notebook may require the corresponding dataset to be downloaded and the file path adjusted when running outside the original Kaggle environment.

## How to Explore the Project

1. Open `global-superstore-eda (1).ipynb`.
2. Review the data-quality and preparation sections first.
3. Continue through the KPI, product, geographic, customer, discount, shipping, and correlation analyses.
4. Review the final conclusion for the main findings and areas for further investigation.

## Limitations

This project is an **exploratory data analysis**, not a causal or predictive model.

In particular:

- Correlations should not be interpreted as causal relationships.
- Aggregate discount/profit patterns do not prove that discounting caused losses.
- Absolute sales and profit do not provide the complete picture of market attractiveness; profit margin and other operational factors should also be considered.
- Further statistical analysis would be required to isolate the effect of individual business factors.

## Author

**Sachin Singh**

GitHub: [SachinSingh-01](https://github.com/SachinSingh-01)
