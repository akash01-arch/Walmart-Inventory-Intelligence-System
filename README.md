# Walmart Inventory & Sales Intelligence Analysis

## Project Overview

This project analyzes Walmart retail sales, inventory, demand forecasting, promotion performance, supplier risk, customer behavior, and store-level performance using **Python, SQL, and exploratory data analysis**.

The goal of this project is to solve real-world business questions that a retail analytics team would face, such as:

- Which stores generate the highest and lowest revenue?
- Which products are at risk of stockout?
- Are promotions increasing revenue or creating inventory pressure?
- Which suppliers need operational review?
- Where is demand forecasting failing?
- Which customer segments should Walmart target?

> Note: This project is created for learning and portfolio purposes using a sample Walmart-style dataset. It is not an official Walmart project.

---

## Business Problem

Walmart wants to improve sales performance, reduce stockout risk, optimize promotions, and improve demand forecasting across stores and product categories.

The business needs a data-driven analysis to identify:

- High-performing and low-performing stores
- Revenue-driving products and categories
- Inventory shortage risks
- Forecasting errors
- Promotion effectiveness
- Supplier performance issues
- Customer segments with high revenue potential

---

## Tools & Technologies Used

- **Python**: Data cleaning, preprocessing, feature engineering, EDA
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical operations
- **Matplotlib & Seaborn**: Data visualization
- **MySQL**: Business analysis using SQL queries
- **SQLAlchemy / PyMySQL**: Python-to-MySQL connection
- **Jupyter Notebook**: Development and analysis environment
- **Git & GitHub**: Version control and project publishing

---
## Notebook Description

### 1. Data Cleaning & Preprocessing

File: `01_walmart_data_cleaning_preprocessing.ipynb`

This notebook focuses on preparing the raw dataset for analysis.

Key tasks performed:

- Loaded Walmart sales dataset
- Checked missing values and duplicate records
- Converted `transaction_date` into proper date format
- Created revenue column using `quantity_sold * unit_price`
- Created forecast error columns
- Created inventory risk and understock indicators
- Checked abnormal values in price, quantity, inventory, and demand columns
- Prepared cleaned dataset for SQL and EDA analysis

---

### 2. SQL Business Analysis

File: `02_walmart_sql_business_analysis.ipynb`

This notebook uses MySQL queries through Python to solve real-world business questions.

Analysis areas:

- Executive KPI summary
- Sales performance analysis
- Store performance analysis
- Inventory risk analysis
- Demand forecasting accuracy
- Promotion effectiveness
- Customer loyalty analysis
- Supplier and reorder analysis
- Weather and holiday impact analysis
- Final business recommendations

---

### 3. Exploratory Data Analysis

File: `03_walmart_exploratory_data_analysis.ipynb`

This notebook focuses on visual analysis and business interpretation.

EDA operations performed:

- Revenue distribution analysis
- Monthly revenue trend
- Category-wise revenue and stockout analysis
- Store scorecard analysis
- Promotion impact analysis
- Holiday impact analysis
- Customer segment revenue analysis
- Product revenue ranking
- Store attention and risk analysis

---

## Dataset Overview

The dataset contains **5,000 transaction records** with sales, inventory, customer, supplier, promotion, weather, and demand forecasting information.

Important columns include:

- `transaction_id`
- `customer_id`
- `product_id`
- `product_name`
- `category`
- `quantity_sold`
- `unit_price`
- `transaction_date`
- `store_id`
- `store_location`
- `inventory_level`
- `reorder_point`
- `supplier_id`
- `supplier_lead_time`
- `customer_age`
- `customer_income`
- `customer_loyalty_level`
- `payment_method`
- `promotion_applied`
- `promotion_type`
- `weather_conditions`
- `holiday_indicator`
- `stockout_indicator`
- `forecasted_demand`
- `actual_demand`
- `revenue`
- `forecast_error`

---

## Key Business Questions Solved

### Sales Performance

- What is the total revenue and transaction count?
- Which category generates the highest revenue?
- Which product generates the highest revenue?
- Which store location performs best and worst?
- What is the monthly revenue trend?
- Which weekday generates the highest sales?

### Inventory Risk

- What is the overall stockout rate?
- Which stores have the highest stockout risk?
- Which products are below reorder point?
- Which products have high demand but low inventory?
- Which products should be reordered immediately?

### Demand Forecasting

- What is the average forecast error?
- Which products have the highest forecast error?
- Which stores have the highest forecast error?
- Is Walmart under-forecasting or over-forecasting demand?
- Is forecast error higher during holidays or promotions?

### Promotion Analysis

- Do promotions increase revenue?
- Do promotions increase stockout risk?
- Which promotion type performs best?
- Do promotions perform better during holidays?

### Customer Analysis

- Which customer loyalty level generates the most revenue?
- Which payment method is most used by customers?
- Which customer group should be targeted?

### Supplier Analysis

- Which suppliers have high lead time and high stockout count?
- Which supplier-product combinations are risky?
- Which suppliers need attention?

---

## Key Insights

### Executive KPIs

- Total Revenue: **$15.26M**
- Total Transactions: **5,000**
- Total Quantity Sold: **14,914 units**
- Average Transaction Value: **$3,052.72**
- Overall Stockout Rate: **51.86%**
- Average Forecast Error Percentage: **59.93%**

### Sales Insights

- **Electronics** generated the highest revenue with approximately **$7.94M**.
- **Appliances** generated approximately **$7.32M**.
- **TV** was the highest revenue-generating product by product name.
- **Los Angeles, CA** was the best-performing store location with approximately **$3.28M** revenue.
- **Dallas, TX** generated the lowest revenue among store locations with approximately **$2.90M**.
- **Thursday** generated the highest weekday revenue.
- **August** recorded the highest monthly revenue.

### Inventory & Stockout Insights

- The overall stockout rate is high at **51.86%**, which shows a serious inventory planning issue.
- **New York, NY** had the highest location-level stockout risk.
- Several products had actual demand greater than available inventory, showing high understock risk.
- Products such as **Camera, Laptop, Headphones, Fridge, and TV** appeared in high-demand and low-inventory analysis.

### Forecasting Insights

- Average forecast error percentage is **59.93%**, which means demand forecasting needs improvement.
- Walmart is slightly more under-forecasting than over-forecasting demand.
- Under-forecasted records: **51.10%**
- Over-forecasted records: **48.72%**
- Forecast error was slightly higher during holidays than non-holidays.

### Promotion Insights

- Transactions with promotions generated approximately **$8.06M** revenue.
- Transactions without promotions generated approximately **$7.20M** revenue.
- Promotions increased revenue, but also slightly increased stockout risk.
- Promotion stockout rate: **52.51%**
- Non-promotion stockout rate: **51.15%**

### Customer Insights

- **Platinum loyalty customers** generated the highest revenue.
- **Credit Card** was the most used payment method.
- **Digital Wallet** contributed the highest total revenue among payment methods.
- High-income middle-aged Platinum customers showed strong targeting potential.

### Holiday & Weather Insights

- Holiday revenue was slightly higher than non-holiday revenue.
- Holiday stockout rate was also slightly higher, showing extra inventory pressure during holidays.
- Sunny weather generated the highest revenue.
- Rainy weather had the highest stockout rate.

---

## Business Recommendations

1. **Improve inventory planning for high-demand products**
   - Products with high actual demand and low inventory should be prioritized for immediate reorder.

2. **Reduce stockout risk in high-risk stores**
   - New York and other high-stockout locations need better inventory allocation and reorder planning.

3. **Improve demand forecasting accuracy**
   - Forecast error is too high, especially for products such as Laptop, Fridge, Camera, Tablet, and Headphones.

4. **Optimize promotional strategy**
   - Promotions increase revenue, but they also increase stockout risk. Walmart should align promotions with inventory availability.

5. **Review suppliers with high lead time and stockout cases**
   - Suppliers with repeated stockout issues and high lead times should be reviewed for reliability.

6. **Focus on Electronics category**
   - Electronics is the highest revenue-generating category and should receive stronger inventory and marketing focus.

7. **Target high-value customer segments**
   - Platinum loyalty customers and high-income customer groups should be targeted with personalized offers.

---

## Skills Demonstrated

- Data cleaning and preprocessing
- Feature engineering
- SQL business analysis
- KPI creation
- Exploratory data analysis
- Inventory risk analysis
- Forecasting error analysis
- Promotion performance analysis
- Customer segmentation
- Supplier risk analysis
- Business insight generation
- Data storytelling for decision-making

---

## How to Run This Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/walmart-inventory-intelligence-system.git
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run notebooks in order

```text
01_walmart_data_cleaning_preprocessing.ipynb
02_walmart_sql_business_analysis.ipynb
03_walmart_exploratory_data_analysis.ipynb
```

---

## Future Improvements

- Build an interactive Power BI dashboard
- Add automated SQL scripts by analysis topic
- Add more advanced customer segmentation
- Add inventory reorder simulation
- Add forecasting model comparison in a separate advanced version
- Create a final business presentation for stakeholders

---

## Author

**Akash More**  
Aspiring Data Analyst  
Skills: Python, SQL, Excel, Power BI, Data Analysis, Business Intelligence

---

## Project Status

Completed: Data Cleaning, SQL Analysis, EDA, KPI Analysis, Business Recommendations  
Next Step: Power BI Dashboard and Final GitHub Project Polish
