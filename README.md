# Power_BI---Automotive-Market-Performance-Dashboard-Power-BI-
# 🚗 Automotive Market Performance Dashboard (Power BI)

This project provides a comprehensive analysis of the global automotive market using **Power BI**.  
It focuses on **sales performance, brand comparison, fuel type trends, CO₂ emissions**, and **country-level market differences**.  
The dashboard is fully interactive and supports decision-making for pricing, market strategy, and sustainability initiatives.

---

## 📂 Dataset
**File:** `random_auto_dataset.csv`  
Contains vehicle attributes such as Brand, Country, Fuel Type, Horsepower, Price, CO₂ Emissions, and Sales Volume.

---

## 🧠 Key Business Insights

| Topic | Insight |
|------|---------|
| Sales Performance | Volkswagen, Hyundai, and Mercedes lead global unit sales. |
| Pricing Strategy | Premium brands show higher pricing and horsepower positioning. |
| Fuel Mix Trends | Hybrid and Electric vehicles show continuous growth. |
| CO₂ Emissions | Diesel vehicles produce the highest CO₂ per km on average. |
| Regional Variation | Price and sales volume vary significantly across markets. |

---

## 📊 Dashboard Pages

| Page | Focus Area | Key Visuals |
|------|------------|-------------|
| **1. Sales Overview** | Market performance summary | KPI Cards, Sales Trend, Sales by Brand |
| **2. Brand Comparison** | Competitor analysis | Market Share %, Price vs Horsepower, Brand Ranking |
| **3. Fuel Mix & Emissions** | Powertrain sustainability insights | Fuel Mix Trend, CO₂ Comparison, Fuel Mix % |
| **4. Country Performance** | Geographic market insights | Sales Map, Avg Price by Country, Country Sales Matrix |

---

## 🔢 Core DAX Measures

```DAX
Total Units = SUM(random_auto_dataset[Sales_Volume])

Total Revenue = SUMX(
    random_auto_dataset,
    random_auto_dataset[Sales_Volume] * random_auto_dataset[MSRP_USD]
)

Average Price = DIVIDE([Total Revenue], [Total Units])

Fuel Mix % = 
DIVIDE(
    [Total Units],
    CALCULATE([Total Units], ALL(random_auto_dataset[Fuel_Type]))
)

🛠 Tools Used

Power BI Desktop

DAX

CSV / Excel

Data Visualization & Business Analytics

🚀 Usage Instructions

Clone the repository

Open the .pbix file in Power BI Desktop

Load the dataset if prompted

Use slicers (Brand, Country, Fuel Type, Month) to explore insights

📬 Contact

LinkedIn: (https://www.linkedin.com/in/ankur-verma-61416362/)
Email: (ankuroberoi017@gmail.com)
