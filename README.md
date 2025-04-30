# 📊 Shop Sales Analysis Project

This project focuses on analyzing store sales data using Python's **Pandas** library. The goal is to understand sales trends over different time periods such as months and years.

## 📁 Dataset

The dataset used in this project is named `storedataset.csv` and contains **9800 rows** and **18 columns** related to customer orders, including:

- Order ID, Order Date, Ship Date  
- Customer details (ID, Name, Segment, Location)  
- Product details (ID, Category, Sub-Category, Name)  
- Sales amount and region  

Missing values were handled by replacing null postal codes with `'no exist'`.

## 📅 Time-Based Sales Analysis

The `Order Date` column was converted to `datetime` format, and new time-related columns were extracted:

- `Year`  
- `Month`  
- `YearMonth` (for monthly grouping)

### 📈 Monthly Sales Trend

Sales were grouped by `YearMonth` to observe trends:

```python
monthly_sales = df.groupby('YearMonth')['Sales'].sum()
```

### 📉 Yearly Sales Summary

```python
yearly_sales = df.groupby('Year')['Sales'].sum()
```

### 📊 Monthly Average Sales

```python
monthly_avg = df.groupby('Month')['Sales'].mean()
```

## 🔍 Key Insights

- The highest annual sales occurred in **2018**.
- Certain months consistently showed higher average sales.
- Sales trends fluctuated over the years, indicating possible seasonal patterns.

## 🛠 Tools Used

- **Python**
- **Pandas**
- **Jupyter Notebook**
## 📁 Dataset

The dataset used in this project is from Kaggle and is not included in this repository due to license restrictions.

You can download it manually from the link below (Kaggle account required):

🔗 [Download Global Weather Dataset from Kaggle](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)

Once downloaded, rename the file (if needed) to `storedataset.csv` and place it in the project root directory.

