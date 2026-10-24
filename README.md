# User Retention Analysis

A comprehensive data analysis project focused on understanding customer behavior, calculating retention rates, and visualizing user cohorts over time using Python and Pandas.

## 📌 Project Overview
User retention is a critical metric for e-commerce and subscription businesses. This project analyzes transactional data from an online retail dataset to track user activity, compute monthly retention rates, and visualize cohort behavior via heatmaps.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python 3.x
- **Data Manipulation:** `pandas`, `numpy`
- **Date & Time Handling:** `datetime`
- **Statistical Analysis:** `scipy.stats` (Z-score for outlier removal)

---

## 🔍 Workflow & Methodology

1. **Environment & Package Setup:**
   - Imported required data analysis libraries (`pandas`, `numpy`, `datetime`).

2. **Data Cleaning & Preprocessing:**
   - Handled missing values (removed rows without `customer_id` or `product_name`).
   - Standardized `product_name` to lowercase and mapped the most frequent name per `product_code`.
   - Converted `order_date` to `datetime` format and generated `year_month` periods.
   - Identified order status (`delivered` vs. `cancelled` based on order ID prefixes).
   - Calculated total transactional `amount` (`quantity * price`).
   - Removed test entries, negative prices, and statistical outliers (Z-score threshold < 3).

3. **Cohort & Retention Analysis:**
   - **Monthly Aggregation:** Grouped transactions by user and month to get distinct order counts.
   - **Cohort Identification:** Determined each user's first purchase month (`cohort`).
   - **Period Calculation:** Calculated month intervals (`period_num`) relative to the cohort start date.
   - **Pivot Table:** Built a pivot matrix tracking unique active users across period numbers.
   - **Retention Rate Calculation:** Calculated percentage retention relative to the initial cohort size.

---

## 🚀 How to Run locally

### 1. Prerequisites
Ensure you have Python installed, then install the required dependencies:
```bash
pip install pandas numpy scipy
```

### 2. Run the Notebook
1. Place the dataset (`Online Retail Data.csv`) in the root project directory.
2. Open Jupyter Notebook / JupyterLab or Google Colab.
3. Run `User_Retention_Analysis.ipynb` step-by-step.

---

## 👤 Author
**Meuthia Evawani Sabilla**  
*Project completed as part of the MySkill Data Analysis Program.*
