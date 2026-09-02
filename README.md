# 🚗 Car Sales Data Analysis | Excel

## 📌 Project Overview

This project analyzes car sales data using **Microsoft Excel** to evaluate sales performance, customer behavior, dealer performance, vehicle characteristics, and the factors affecting sales revenue.

The project follows a complete **Data Analysis workflow**, starting from data understanding and quality validation, followed by data preparation using Power Query, calculated columns, exploratory analysis, Pivot Tables, visualizations, and an interactive Excel Dashboard.

The main goal is to transform raw sales data into meaningful **business insights and recommendations** that can support better understanding of sales performance and customer behavior.

---

# 🎯 Business Objectives

The main objectives of this analysis are to:

* Evaluate overall sales performance and revenue trends.
* Identify the strongest companies and vehicle models.
* Understand the relationship between sales volume and average selling price.
* Identify top-performing cities and dealers.
* Analyze customer purchasing behavior.
* Compare sales across different customer income groups.
* Analyze vehicle characteristics such as body style, transmission, engine, and color.
* Evaluate car affordability relative to customer annual income.
* Identify important sales patterns and trends.
* Extract actionable business insights from the data.

---

# ❓ Business Questions

The analysis was designed around the following business questions:

### Sales Performance

* How are sales and revenue changing over time?
* Which months generate the highest and lowest sales?
* Is revenue growth driven by sales volume or average selling price?

### Company & Model

* Which companies generate the highest sales volume and revenue?
* Does higher sales volume always result in higher revenue?
* Which vehicle models perform best?
* How does average selling price affect revenue?

### Location & Dealers

* Which cities generate the highest sales?
* Which dealers generate the highest revenue?
* Is revenue heavily concentrated among a small number of dealers?

### Customers

* Which customers generate the highest revenue?
* How are sales distributed by gender?
* How are sales distributed across customer income groups?

### Vehicle Characteristics

* Which body styles are most popular?
* Which transmission type generates more sales?
* Does engine type provide additional analytical value?
* Which car colors are most common?

### Affordability

* How does car price compare with customer annual income?
* What percentage of purchases are relatively affordable compared with customer income?
* How many purchases have a very high car-price-to-income ratio?

---

# 📂 Dataset

The dataset contains information related to:

* Car sales
* Customers
* Customer income
* Dealers
* Companies
* Vehicle models
* Vehicle characteristics
* Sales prices
* Locations
* Dates

### Original Columns

```text
Car_id
Date
Customer Name
Gender
Annual Income
Dealer_Name
Company
Model
Engine
Transmission
Color
Price ($)
Dealer_No
Body Style
Phone
Dealer_Region
```

---

# 🧹 Data Quality & Cleaning

The original dataset was already in **good condition** and did not contain **NULL values** that required treatment.

Therefore, the data cleaning stage was mainly focused on **data validation and preparation rather than fixing major data-quality problems**.

### Data Preparation Steps

* Checked the dataset structure and columns.
* Verified data types.
* Confirmed that there were no NULL values requiring imputation.
* Reviewed data consistency.
* Prepared date fields for time-based analysis.
* Transformed the dataset using **Power Query**.
* Created additional calculated columns for deeper analysis.
* Prepared the final dataset for Pivot Tables and Dashboard development.

This approach ensured that the dataset was reliable and ready for analysis before creating the visualizations and business insights.

---

# 📊 Derived Columns

Six additional analytical columns were created to improve the analysis.

| Derived Column                 | Purpose                                                                        |
| ------------------------------ | ------------------------------------------------------------------------------ |
| **Year**                       | Analyze sales performance by year                                              |
| **Month**                      | Analyze monthly sales patterns and seasonality                                 |
| **Year-Month**                 | Create a continuous monthly sales trend while preserving the year              |
| **Income Group**               | Segment customers based on annual income                                       |
| **Car_income_per**             | Measure car price relative to annual income                                    |
| **Income Affordability Group** | Classify the car-price-to-income ratio into Low, Moderate, High, and Very High |

### Car Income Percentage

The following metric was created:

**Car_income_per = Price ÷ Annual Income**

The resulting values were classified into:

* Low
* Moderate
* High
* Very High

This metric was used to evaluate vehicle affordability relative to customer income.

---

# 🔎 Exploratory Data Analysis

## 📅 Time Analysis

Sales were analyzed using:

* Year
* Month
* Year-Month

### Key Findings

Revenue in **2023 increased by approximately 23.59% compared with 2022**.

The increase was mainly associated with **higher sales volume rather than a significant increase in average selling price**.

Monthly analysis also showed that:

* **January** was one of the weakest months.
* **September** was one of the strongest months.
* **November and December** also showed relatively strong sales performance.

This indicates that sales performance varies across different months.

---

# 🏢 Company Analysis

Companies were evaluated using:

* Sales Volume
* Sales Revenue
* Average Selling Price

### Key Findings

**Chevrolet** recorded the highest sales volume and revenue among the analyzed companies.

The analysis also revealed an important relationship between volume and revenue.

**Ford sold fewer cars than Dodge but generated higher revenue because its average selling price was higher.**

This demonstrates that:

> **Sales volume alone does not determine revenue. Average selling price also plays an important role.**

---

# 🚘 Model Analysis

Vehicle models were analyzed using:

* Sales Volume
* Sales Revenue
* Average Selling Price

The analysis showed that revenue performance is influenced by both:

* Number of vehicles sold
* Average selling price

Therefore, a model with fewer sales can potentially generate higher revenue if its average selling price is significantly higher.

---

# 🌍 City Analysis

## Top-performing City

**Austin** recorded the highest sales performance:

* **4,135 cars sold**
* **$117.19M revenue**
* **$28,341.60 average selling price**

The average selling price in Austin was close to the overall average of approximately **$28,090.25**.

This indicates that Austin's leading performance was mainly driven by **high sales volume rather than significantly higher vehicle prices**.

---

# 🏪 Dealer Analysis

Dealers were compared based on:

* Sales Volume
* Sales Revenue

## Top Dealer

**Rabun Used Car Sales** generated the highest sales revenue:

**$37.46M**

However, the revenue differences among the leading dealers were relatively moderate.

This suggests that sales performance is **reasonably distributed among the top-performing dealers rather than being dominated by a single dealer**.

---

# 👥 Customer Analysis

## Top Customers

Customer revenue was analyzed to identify the highest-value customers.

### Top Customer

**Emma** generated the highest revenue among the Top 10 customers:

* **$2.80M revenue**
* **90 cars purchased**

The revenue differences among the top customers were relatively moderate, indicating that revenue is **not heavily concentrated in a single customer**.

---

# ⚥ Gender Analysis

Sales were analyzed by customer gender.

### Results

* **Male:** 18,798 cars — approximately **78.6%**
* **Female:** 5,108 cars — approximately **21.4%**

Male customers represent the majority of vehicle sales in this dataset.

---

# 💰 Income Analysis

Customers were divided into four income groups:

* Low
* Lower-Middle
* Upper-Middle
* High

### Key Findings

Sales were **almost evenly distributed across the four income groups**, with each segment contributing approximately 25% of total vehicle sales and revenue.

This indicates that sales are **not heavily concentrated within a specific customer income segment**.

---

## 💵 Income vs Average Car Price

Average vehicle prices were very similar across all income groups.

The average price ranged approximately from:

**$27,954 → $28,289**

This suggests that customer annual income has a **limited relationship with the average price of vehicles purchased** in this dataset.

---

# 📈 Car Price vs Annual Income

The `Car_income_per` metric was created using:

**Price ÷ Annual Income**

The resulting values were categorized into four affordability groups:

* Low
* Moderate
* High
* Very High

### Key Finding

The majority of purchases fall into the **Low** affordability group:

* **18,622 cars**
* **77.9% of total sales**

Meanwhile:

* **4,793 cars**
* **20.1%**

fall into the **Very High** group, where the car price exceeds the customer's annual income.

This provides an additional perspective on customer purchasing power and vehicle affordability.

---

# 🚙 Vehicle Characteristics

## Body Style

**SUV** was the top-selling body style:

* **6,374 cars sold**
* **$170.62M revenue**

It was followed closely by:

**Hatchback**

* **6,128 cars sold**
* **$166.23M revenue**

SUV leads both sales volume and revenue, indicating that its strong revenue performance is primarily driven by its higher sales volume.

---

## ⚙️ Transmission

Automatic transmission vehicles recorded higher sales than manual vehicles.

### Automatic

* **12,571 cars**
* **$355.11M revenue**

### Manual

* **11,335 cars**
* **$316.41M revenue**

Automatic vehicles lead in both sales volume and revenue, although the difference is relatively moderate.

This indicates that **both transmission types have significant demand**.

---

## 🔧 Engine

Engine categories were also analyzed.

However, the engine distribution showed a similar pattern to the transmission analysis and did not provide significant additional analytical value.

Therefore, **Engine was not considered a high-value variable for the final business analysis**.

This demonstrates an important analytical principle:

> Not every available column needs to be included in the final analysis if it does not provide meaningful additional insights.

---

# 🎨 Color Analysis

The most common vehicle colors were:

1. **Pale White** — 11,256 sales
2. **Black** — 7,857 sales
3. **Red** — 4,793 sales

Pale White was the most common car color in the dataset.

---

# 💡 Key Business Insights

### 1. Revenue Growth

Revenue increased by **23.59% from 2022 to 2023**, mainly due to higher sales volume rather than higher average prices.

### 2. Volume vs Revenue

Higher sales volume does not always mean higher revenue.

Ford generated more revenue than Dodge despite selling fewer vehicles because Ford had a higher average selling price.

### 3. City Performance

Austin was the strongest city, with **4,135 cars sold and $117.19M revenue**, mainly driven by high sales volume.

### 4. Dealer Performance

Rabun Used Car Sales generated the highest dealer revenue at **$37.46M**, while the leading dealers showed relatively moderate revenue differences.

### 5. Customer Concentration

Emma generated **$2.80M from 90 cars**, but revenue was not heavily concentrated in a single customer.

### 6. Gender Distribution

Male customers represented approximately **78.6% of total vehicle sales**, compared with 21.4% for female customers.

### 7. Income Segmentation

Sales were distributed relatively evenly across the four income groups, indicating that no single income segment dominates the market.

### 8. Vehicle Affordability

Approximately **77.9% of purchases** fell into the Low affordability group, while **20.1%** fell into the Very High group.

### 9. Body Style

SUV was the leading body style in both sales volume and revenue.

### 10. Transmission

Automatic vehicles slightly outperformed manual vehicles in both volume and revenue.

### 11. Customer Income vs Vehicle Price

Average vehicle prices were very similar across income groups, suggesting that income has limited influence on the average price of vehicles purchased.

### 12. Variable Selection

Engine did not provide significant additional analytical value compared with other vehicle characteristics and therefore was not emphasized in the final analysis.

---

# 📊 Dashboard

An interactive **Excel Dashboard** was created to present the most important KPIs, trends, and business insights in a clear and visual format.

## Dashboard Preview

## 🎥 Dashboard Demo

[▶️ Watch the Dashboard Demo](dashboard_demo.mp4)

The dashboard provides an overview of:

* Total Sales
* Total Cars Sold
* Average Car Price
* Sales Trends
* Company Performance
* Dealer Performance
* Customer Analysis
* Vehicle Characteristics
* Income Analysis

---

# 🎯 Business Recommendations

Based on the analysis, several recommendations can be considered:

### 1. Focus on Sales Volume

Since revenue growth was mainly driven by higher sales volume, strategies that increase the number of vehicles sold can have a significant impact on revenue.

### 2. Monitor Average Selling Price

Sales performance should be evaluated using both **sales volume and average selling price**, since higher volume does not always result in higher revenue.

### 3. Learn From High-Performing Cities

Austin's strong performance suggests that successful strategies in high-performing cities could be studied and potentially applied to other markets.

### 4. Plan Around Seasonal Demand

The difference between weaker months such as January and stronger months such as September, November, and December suggests an opportunity to align marketing campaigns and inventory planning with seasonal demand.

### 5. Maintain Dealer Performance

Since revenue is relatively distributed among leading dealers, maintaining strong performance across multiple dealers can reduce dependency on a single sales channel.

### 6. Focus on Popular Vehicle Types

SUVs and automatic vehicles show strong demand and may deserve additional attention in inventory and sales planning.

### 7. Use Customer Segmentation

Since sales are relatively evenly distributed across income groups, targeting only one income segment may limit potential sales opportunities.

---

# 🧰 Tools & Technologies

* **Microsoft Excel**
* **Power Query**
* **Pivot Tables**
* **Calculated Columns**
* **Excel Charts**
* **Data Visualization**
* **Interactive Dashboard**

---

# 📁 Project Structure

```text
Car_Sales_Analysis/
│
├── Car_Sales_Analysis.xlsx
├── car-sales-dashboard.png
├── dashboard_demo.mp4
└── README.md
```

---

# 🏁 Conclusion

This project demonstrates a complete **Excel-based Data Analysis workflow**, from understanding and validating the raw dataset to data preparation, calculated columns, exploratory analysis, Pivot Tables, visualization, and dashboard development.

The original dataset was already in good condition and contained no NULL values requiring treatment. Therefore, the cleaning stage focused mainly on **validation, consistency checks, data types, and preparing the dataset for analysis**.

The analysis demonstrates how Excel can be used not only for reporting, but also for identifying meaningful **business patterns, relationships, and actionable insights**.

The project also highlights an important part of data analysis: **analytical value is more important than analyzing every available column**. Variables should be included when they provide meaningful information that can support business understanding or decision-making.

---

## 👨‍💻 Project Author

**Fares Sameh**

Data Analysis | Excel | SQL | Python | Power BI

[GitHub Profile](https://github.com/fs0194771-png)
