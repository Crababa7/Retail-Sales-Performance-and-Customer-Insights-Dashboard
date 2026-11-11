# Retail Sales Performance & Customer Insights Dashboard

An interactive Power BI report that turns retail sales data into answers a business can act on: where revenue comes from, which products and customers matter most, and how sales move over time.

## Business questions
- How are we performing overall (sales, profit, margin, orders, customers)?
- Which regions, products, and categories drive revenue and profit?
- Who are the most valuable customers and segments?
- How do sales change month to month, and why did September come in low?

## Report pages
    Page	                                                            What it answers
- Sales Dashboard	                Headline KPIs, monthly trend, sales by region and category, with Region and Category slicers
  <img width="991" height="553" alt="Screenshot 2026-11-11 171346" src="https://github.com/user-attachments/assets/84d2664c-1b97-4abc-a39e-a9d4434bbf66" />

- Region Dashboard	              Sales, profit, profit margin, and customers by region, with a Month slicer
  <img width="1021" height="562" alt="Screenshot 2026-11-11 165812" src="https://github.com/user-attachments/assets/355605bc-b6d3-4fa1-9448-d55e131207c4" />

- Product Dashboard	              Sales by product, profit by product and category, profit margin by product
  <img width="1056" height="598" alt="Screenshot 2026-11-11 165735" src="https://github.com/user-attachments/assets/b2e040ed-e02d-4f23-a541-edd5000fda82" />

- Customer Dashboard	            Top 10 customers by sales and profit, revenue by customer segment
  <img width="988" height="568" alt="Screenshot 2026-11-11 165724" src="https://github.com/user-attachments/assets/a0643721-c433-4282-b627-15f9da53ea49" />

- Time Intelligence Dashboard	    Month-over-month growth, current vs previous month sales, monthly trend
<img width="999" height="573" alt="Screenshot 2026-11-11 165607" src="https://github.com/user-attachments/assets/fc209b65-ab41-4e1b-ad4d-af5c5f179860" />


# Data Cleaning & Preparation Process
 
**Tool:** Power Query (Power BI)


## Headline numbers
 
| Metric | Value |
|---|---|
| Total sales | ₦3.12bn |
| Total profit | ₦873.9M |
| Profit margin | 28% |
| Total orders | ~8K |
| Total customers | 300 |

---
 
## Headline numbers
 
| Metric | Value |
|---|---|
| Total sales | ₦3.12bn |
| Total profit | ₦873.9M |
| Profit margin | 28% |
| Total orders | ~8K |
| Total customers | 300 |
 
---
 
## Key findings
 
**Regions**
- South East (₦0.73bn), South West (₦0.71bn), and South South (₦0.69bn) bring in about two-thirds of total sales. North West (₦0.52bn) and North Central (₦0.47bn) trail.
- Profit margin is about 28% in **every** region, so differences in profit between regions come from sales volume, not pricing or cost.
**Products and categories**
- Electronics (₦1.30bn) and Furniture (₦1.07bn) generate roughly three-quarters of sales and profit. Accessories, Networking, and Power are small by comparison.
- Laptop (₦0.44bn) and Conference Table (₦0.41bn) are the top sellers. Conference Table is the top profit earner (~₦119M), ahead of Laptop (~₦110M).
- Margin runs inversely to sales: the biggest sellers have the **lowest** margins (Laptop, Smartphone, Monitor at about 25%), while small accessories such as Mouse (38%), Extension Box (37%), and Headset (36%) have the highest.
**Customers**
- SME is the largest segment (43.8% of revenue), followed by Corporate (30.8%) and Individual (25.5%).
- Customer C0294 is the top customer by both sales (~₦17M) and profit (~₦4.8M).
**Time trends**
- Monthly sales range from about ₦0.38bn at the peak (March) down to ₦0.15bn in September.
- Among the months, January to June sit around ₦0.32-0.38bn, while July to December sit around ₦0.15-0.19bn.
  
---
 
## Data model
 
Star schema built in Power BI:
 
- **Fact_Sales:** transactions
- **Dim_Date:** Date, Day, DayName, Month, MonthNumber, Quarter, Year, YearMonth
**DAX measures used:** Total_Sales, Total_Cost, Total_Profit, Profit_Margin, Total_Orders, Total_Customers, Total_Quantity, previousMonthSales, Sales_Growth, Sales_Growth%
 
 ```DAX
Sales_Growth% =
DIVIDE ( [Total_Sales] - [previousMonthSales], [previousMonthSales] )
```

 ## Business recommendations 
 
1. **Investigate the volume decline** in later months before drawing conclusions, starting with order counts and data completeness.
2. **Protect margin on high-volume electronics** (Laptop, Smartphone, Monitor), where margins are lowest at ~25%.
3. **Grow accessories** (Mouse, Extension Box, Headset), which carry the highest margins but small sales.
4. **Target North West and North Central** with promotions or distribution work, since margins are equal to other regions but volume lags.
5. **Focus retention on SME customers,** the largest revenue segment.
---

## Skills demonstrated
 
Power Query · DAX · Star-schema data modeling · Time intelligence · KPI design · Interactive slicers · Data storytelling · Bookmarks · Custom tooltips  
---

 
