# Data Science Foundations & Visualization

---

## Objective

* Apply data cleaning and exploratory data analysis techniques to a “dirty” dataset
* Gain insights through meaningful visualizations
* Build familiarity with foundational data science workflows using Python, pandas, Matplotlib, and Seaborn

## 1. Dataset Description

The dataset used in this task is called **The Dirty Cafe Sales dataset**. It contains **10,000 rows** and **8 columns** of synthetic data representing sales transactions in a café. This dataset is intentionally “dirty,” with missing values, inconsistent formatting, and injected errors to provide a realistic scenario for data cleaning and exploratory data analysis (EDA).

## 2. Data Cleaning

Data cleaning steps performed:

* **Missing value handling**: identified and treated null entries via imputation or removal.
* **Duplicate removal**: detected and dropped duplicate records.
* **Formatting adjustments**: standardized date and string formats.
* **Outlier detection/remove**: used boxplots and the IQR method to flag and handle extreme values.

## 3. Exploratory Data Analysis

After cleaning, EDA was applied to uncover patterns and relationships:

* Computed **summary statistics** (mean, median, standard deviation) for each variable.
* Analyzed **distributions** with histograms and density plots.
* Examined **pairwise correlations** to identify strong relationships.
* Explored **time trends** by aggregating monthly totals.

## 4. Data Visualizations

* Boxplot to detect outliers
  ![Boxplot of Quantity](images/boxplot_quantity.png)
  reveals no outliers in the quantity column and highlights extreme values in total\_spent

* Correlation matrix
  ![Correlation Matrix](images/correlation_matrix.png)
  shows strong positive correlation between quantity & total\_spent, and price\_per\_unit & total\_spent, with almost no correlation between quantity & price\_per\_unit

* Bar chart for item comparison
  ![Item Comparison Bar Chart](images/item_bar_chart.png)
  identifies juice as the most purchased item and drinks as the most popular category

* Line graph for monthly profit trends
  ![Monthly Profit Trends](images/monthly_profit_trends.png)
  shows february had the highest profit (\~10900), then dropped to \~7250 in march, afterwards it stayed between 7000–7600

* Pairplot of numeric features
  ![Pairplot of Numeric Features](images/pairplot_numeric.png)
  confirms that transaction value rises with quantity and to a lesser extent with unit price, most orders involve 2–4 items

* Bar chart of revenue by weekday
  ![Revenue by Weekday](images/revenue_weekday.png)
  highlights peak sales on monday and shows workdays outperform weekends

* Bar chart of average spend per order by weekday
  ![Avg Spend per Order by Weekday](images/avg_spend_weekday.png)
  shows days with fewer transactions but higher spend, useful for targeting promotions

tools used: pandas, matplotlib, seaborn (in colab)## 5. Project Structure

```text
.
├── data/
│   └── Dirty_Cafe_Sales.csv   # Dirty Cafe Sales dataset (Kaggle)
├── notebooks/
│   └── Task1_EDA.ipynb        # Google Colab notebook performing cleaning & EDA
├── Task1_Report.pdf           # Original report document
└── README.md                  # Project README (this file)
```

## 6. How to Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/USERNAME/REPO_NAME.git
   cd REPO_NAME
   ```
2. **Install dependencies**

   ```bash
   pip install pandas matplotlib seaborn
   ```
3. **Download the dataset**

   * Go to Kaggle: [https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)
   * Download and save `Dirty_Cafe_Sales.csv` into the `data/` directory.
4. **Open the notebook**

   * Launch `notebooks/Task1_EDA.ipynb` in Google Colab or Jupyter.
5. **Run all cells**

   * Execute each cell to perform data cleaning, EDA, and generate visualizations.

## 7. References

1. Ahmed Mohamed. *Cafe Sales Dirty Data for Cleaning Training*. Kaggle.
   [https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)
2. Google Colab notebook:
   [https://colab.research.google.com/drive/1ZuZ1wi1\_XxUNPEDelbT3jM4m-5HEwOpt?usp=sharing](https://colab.research.google.com/drive/1ZuZ1wi1_XxUNPEDelbT3jM4m-5HEwOpt?usp=sharing)
