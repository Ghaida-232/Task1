# Data Science Foundations & Visualization

---

## Objective

* Apply data cleaning and exploratory data analysis techniques to a “dirty” dataset
* Gain insights through meaningful visualizations
* Build familiarity with foundational data science workflows using Python, pandas, Matplotlib, and Seaborn


## 1. Overview 

## 1.1 Dataset Description

  The dataset used in this task is called “The Dirty Cafe Sales dataset” [1]. It contains 
10,000 rows and 8 columns of synthetic data representing sales transactions in a cafe. This 
dataset is intentionally "dirty" with missing values, inconsistent data and errors introduced 
to provide a realistic scenario for data cleaning and exploratory data analysis (EDA). The 
main objective of this task was to apply data analysis and visualization techniques on a 
dataset to gain better understanding about foundations of data science and data 
visualizations. 

## 1.2 Analysis performed 

  Analysis phase is very critical since it gives a lot of useful insight to understand the data 
better and predict the conclusion based on the analysis and even more. For that, I start by 
observing the dataset then cleaning it to be ready for the analysis, cleaning the data 
includes handling the missing values, duplicates, data formatting and solving the outliers. 
After that apply the exploratory data analysis (EDA) technique to gain useful insights and 
then visualize it using google colab (python) and its tools such as Matplotlib and Seaborn. 

## 2. Data Cleaning

Data cleaning steps performed:

* **Missing value handling**: identified and treated null entries via imputation or removal.
* **Duplicate removal**: detected and dropped duplicate records.
* **Formatting adjustments**: standardized date and string formats.
* **Outlier detection/remove**: used boxplots and the IQR method to flag and handle extreme values.

## 3. Exploratory Data Analysis

After cleaning, EDA was applied to uncover patterns and relationships:

1- * Computed **summary statistics** (mean, median, standard deviation) for each variable.


<img width="644" height="363" alt="image" src="https://github.com/user-attachments/assets/922fc198-b3ca-49c5-872f-bd4c2a032f2a" />




2- * Analyzed **distributions** with histograms and density plots.


<img width="739" height="739" alt="image" src="https://github.com/user-attachments/assets/bcd9e600-d4f1-4465-8dd3-88917878dd19" />





3- * Examined **pairwise correlations** to identify strong relationships.


  <img width="509" height="433" alt="image" src="https://github.com/user-attachments/assets/45d6b7ab-41e9-43f0-a100-be0634733ab5" />





4- * Explored **time trends** by aggregating monthly totals.


  <img width="587" height="454" alt="image" src="https://github.com/user-attachments/assets/e253f774-4fa9-4dde-a61e-45e2a05ff954" />




## 4. Data Visualizations

* ## 4.1 Boxplot to detect outliers

<img width="1416" height="676" alt="image" src="https://github.com/user-attachments/assets/43062643-7a38-4c4c-913b-03004c6d7f13" />




* ## 4.2 Correlation matrix
  
 <img width="750" height="540" alt="image" src="https://github.com/user-attachments/assets/71413741-e695-45b9-9aa4-ddd0f7d9113b" />

Useful insights we gain here are:  
- There is a strong positive correlation between ‘quantity’ and ‘total_spend; as quantity increases, total_spent increases.
- There is a strong positive correlation between ‘price_per_unit’ and ‘total_spend’; the more expensive the item, the higher the total spent. 
- There is almost no correlation between ‘quantity’ and ‘price_per_unit’; the number of items bought does not depend on item price. 
- Total spending is influenced by both quantity and item price.



* ## 4.3 Bar chart for item comparison
  
 <img width="1220" height="604" alt="image" src="https://github.com/user-attachments/assets/a7bcbe65-6b62-4c80-b17a-83aea8ca52fd" />

Useful insight we gain here: 
- The most purchased item is juice.  
- The drinks are the most popular in the café. 
- All items appear to be selling consistently. 



* ## 4.4 Line graph for monthly profit trends
  
 <img width="822" height="627" alt="image" src="https://github.com/user-attachments/assets/10b9edaa-1a08-447d-80c7-c97d1d29a81f" />

Useful insight we gain here: 
- The highest profits are recorded in month 2 (February), reaching approximately 10,900. 
- In month 3 (March), profits noticeably decreased to around 7,250 marking a significant 
drop. 
- This decline may indicate the end of a seasonal promotion or temporary customer surge 
in February, or a general decrease in the café’s performance. 
- Most other months maintain consistent performance, with revenue ranging between 7,000 
to 7,600. 
- Despite the early peak, the overall monthly performance is relatively stable after March. 
- These insights help identify potential peak seasons and support better forecasting and 
planning for future sales campaigns. 



* ## 4.5 Pairplot of numeric features
  
 <img width="798" height="758" alt="image" src="https://github.com/user-attachments/assets/697929e9-4f12-4f4b-bdfa-dec5a3510d7d" />

Useful insights we gain here: 
- Higher purchase volume directly increases transaction value.  
- Price per unit also affects total spending, its relationship is weaker.  
- There is no clear link between quantity and price per unit, indicating prices are fixed 
regardless of order size.  
- quantity: Most orders are for 2–4 items.
- price_per_unit: Peaks at 3 and 4.
- total_spent: Right: most purchases are under 15.



  
* ## 4.6 Bar chart of revenue by weekday
  
<img width="806" height="496" alt="image" src="https://github.com/user-attachments/assets/59408e80-0fa4-4039-902a-fb59e69a666a" />

Useful insight we gain here: 
- Analyzing spending by weekday helps identify peak sales, here the result shows high 
performance on Monday. 
- Most total revenue is similar during the week. 
- Workday seems to gain more revenue than the weekend that helps to consider customer 
behavior.

* ## 4.7 Bar chart of average spend per order by weekday
  
<img width="818" height="495" alt="image" src="https://github.com/user-attachments/assets/ebc9f143-0e3a-440f-9897-9a2d00e485cd" />

Useful insights we gain here: 
- Analyzing average spend per order by weekday helps understand how much customers 
typically spend per visit. 
- The result shows that some days have fewer transactions but higher spend per order, 
which can be more profitable. 
- Weekend days may show higher average spend, suggesting customers buy more items or 
high-cost products. 
- This insight supports planning targeted promotions on low-spending days and 
maximizing upselling opportunities on high-spending ones.

tools used in Visualizations: pandas, matplotlib, seaborn (in colab)


## 5. Conclusion

  In this task we performed a comprehensive data cleaning and exploratory data analysis 
(EDA) on a synthetic café sales dataset. The dataset initially included various data quality 
issues such as missing values, inconsistent formatting and incorrect data types, all of 
which were handled through appropriate cleaning techniques. Through descriptive 
statistics and visual analysis, we discovered several useful insights that can help the 
café’s management in making informed decisions regarding promotions, resource 
planning and marketing strategies based on customer behavior trends.  


## 6. Project Structure

```text
.
├── content/
│   └── Dirty_Cafe_Sales.csv   # Dirty Cafe Sales dataset (Kaggle)
├── notebooks/
│   └── Task1_EDA.ipynb        # Google Colab notebook performing cleaning & EDA
└── README.md                  # Project README (this file)
```


## 7. How to Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/Ghaida-232/Task1.git
   cd Task1
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


## 8. References

1. The dataset used in this task: 
https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for
cleaning-training [1]

2.The link of google colab notebook (code): 
https://colab.research.google.com/drive/1ZuZ1wi1_XxUNPEDelbT3jM4m
5HEwOpt?usp=sharing [2]
