# Sales Data Analysis Exploratory Data Analysis(EDA)
A comprehensive end-to-end EDA project using Python, Pandas, Matplotlib, Seaborn, and Plotly
Sales Data Analysis — Exploratory Data Analysis (EDA)

> **A comprehensive end-to-end EDA project using Python, Pandas, Matplotlib, Seaborn, and Plotly**  
> Analysing 1,000 supermarket sales transactions across 3 branches to uncover revenue patterns, customer behaviour, and business insights.

---

## Project Overview

This project performs a full **Exploratory Data Analysis (EDA)** on a supermarket sales dataset to identify sales trends, product performance, and regional insights that support data-driven business decisions.

The analysis covers everything from raw data cleaning to advanced interactive visualisations — structured as a submission for a **Data Analytics Final Project**.

---

## Problem Statement

> *"How can the supermarket chain optimise its sales strategy, product offerings, and customer experience across its three branches to maximise revenue and customer satisfaction?"*

**Key questions answered:**
- Which branch and city generates the highest revenue?
- Which product lines are most and least profitable?
- How do gender and customer type influence purchasing behaviour?
- Is there a relationship between customer rating and total spend?
- Which payment methods are most preferred per branch?

---

##  Repository Structure

```
sales-eda-project/
│
├── Sales_and_E-commerce_python_EDA.xlsx   # Raw dataset (source file)
├── Sales_EDA_Final_Project.ipynb          # Main Jupyter Notebook (full EDA)
└── README.md                              # Project documentation
```

---

##  Dataset Description

| Property | Details |
|---|---|
| **Source** | HuggingFace —  Sales Dataset |
| **Records** | 1,000 rows × 17 columns |
| **Period** | January – March 2019 |
| **Branches** | 3 (Yangon, Mandalay, Naypyitaw) |
| **Missing Values** | None |

**Key columns:**

| Column | Type | Description |
|---|---|---|
| `Branch` / `City` | String | Store location |
| `Customer type` | String | Member or Normal |
| `Gender` | String | Male / Female |
| `Product line` | String | 6 product categories |
| `Unit price` | Float | Price per item (USD) |
| `Quantity` | Int | Units purchased |
| `Total` | Float | Final transaction amount |
| `Payment` | String | Cash / Ewallet / Credit card |
| `Rating` | Float | Customer satisfaction (1–10) |
| `gross income` | Float | Profit per transaction |

---

## Tools & Libraries

| Tool | Purpose |
|---|---|
| **Python 3.x** | Core language |
| **Pandas** | Data loading, cleaning, manipulation |
| **NumPy** | Numerical operations |
| **Matplotlib** | Static visualisations |
| **Seaborn** | Statistical & advanced visualisations |
| **Plotly** | Interactive charts |
| **Jupyter Notebook** | Development environment |

---

##  Steps Followed

1. **Data Loading** — Imported dataset using Pandas; inspected shape, dtypes, and summary stats
2. **Data Pre-processing**
   - Checked and confirmed zero missing values and duplicates
   - Converted Date and Time columns to proper datetime formats
   - Engineered derived features: Month, Hour, Day of week, Day type, Revenue per unit, Customer Satisfaction Level
3. **Exploratory Data Analysis**
   - Univariate, bivariate, and multivariate analysis
   - GroupBy aggregations and pivot tables
   - Correlation analysis
4. **Visualisations** — 14 static plots + 1 interactive Plotly charts
5. **Insight Generation** — 5 key business insights with recommendations

---

## Visualisations

### Static (Matplotlib / Seaborn)
| Visualization Title                                            | Type of Visualization Used                  |
| -------------------------------------------------------------- | ------------------------------------------- |
| Distribution of Product Lines                                  | Count Plot (Bar Chart)                      |
| Customer Type Distribution                                     | Count Plot (Bar Chart)                      |
| Preferred Payment Methods                                      | Count Plot (Bar Chart)                      |
| Customer Gender Count                                          | Count Plot (Bar Chart)                      |
| Customer Rating Distribution                                   | Histogram with KDE (Distribution Plot)      |
| Total Revenue by Branch                                        | Bar Plot                                    |
| Revenue Share by Branch                                        | Pie Chart                                   |
| Revenue by Product Line                                        | Bar Plot                                    |
| Daily Total Sales Trend (Jan – Mar 2019)                       | Line Chart with Area Fill & Rolling Average |
| Temporal Sales Patterns: Revenue Heatmap — Hour × Day          | Heatmap                                     |
| Monthly Revenue Trend by Branch (Jan–Mar 2019)                 | Multi-Line Chart                            |
| Scatter Analysis — Price vs Revenue | coloured by Product line | Scatter Plot                                |
| Scatter Analysis — Price vs Revenue | coloured by Gender       | Scatter Plot                                |
| Correlation Matrix of Numerical Features                       | Correlation Heatmap                         |
| Gender vs Total Spend                                          | Box Plot                                    |


### Interactive (Plotly)
Treemap - Revenue by Branch → Customer Type → Payment

---

## Key Insights

1. **Balanced Branch Performance** — All 3 branches contribute ~33% of total revenue, indicating no single dominant location.
2. **Food & Beverages leads revenue; Health & Beauty leads ratings** — A strong upsell opportunity exists in Health & Beauty.
3. **Peak hours: 10–11 AM, 1 PM, 7 PM** — Staffing and promotions should target these windows.
4. **Rating is independent of spend** — Customer satisfaction is driven by experience, not transaction size (correlation ≈ 0.0).
5. **E-wallets are the dominant payment method** (~34%) — Digital payment incentives could reduce cash-handling costs.

---

##  Recommendations

| # | Recommendation | Rationale |
|---|---|---|
| 1 | Boost Health & Beauty marketing | Highest ratings but not top revenue — untapped potential |
| 2 | Implement loyalty programs for Members | Differentiate Members to increase basket size |
| 3 | Expand E-wallet partner deals | Growing digital payment preference |
| 4 | Train staff on service quality over upselling | Ratings are satisfaction-driven, not spend-driven |
