# Dashboards
Compilation of various dashboards on Power BI and Tableau

# Supply Chain Dashboard 1

## Problem Statement
How did service levels affect contract renewal for customers? This project analyzes key supply chain metrics to understand their impact on customer retention and contract renewals. Built using Excel for data cleaning and Power BI for visualization.

## Key Metrics

- **Line Fill Rate**: % of order lines shipped vs. ordered
- **Volume Fill Rate**: % of total quantity shipped vs. ordered
- **On-Time Rate**: % of orders delivered on time
- **In-Full Rate**: % of orders delivered in full quantity
- **OTIF Rate**: % of orders delivered both on time and in full

## Project Structure
- `data/`: Cleaned Excel dataset
- `powerbi/`: Power BI dashboard and data model documentation
- `insights/`: Analytical write-up and recommendations

## Dashboard Insights
- Line Fill Rate and Volume Fill Rate met targets
- OTIF and On-Time metrics are significantly below target
- Potential causes: poor route optimization, inventory issues, production delays

## Recommendations
- Improve route optimization and vendor selection
- Enhance inventory and production efficiency
- Strengthen vendor relationships
- Investigate reasons for contract discontinuation (pricing, service, logistics)

## How to Use
1. Open `dashboard.pbix` in Power BI from the supplychaindashboard1 folder
2. Review `data_model_overview.md` for structure
3. Explore insights in `service_level_analysis.md`

# Supply Chain Dashboard 2

This project analyzes a mock supply chain dataset from Kaggle and builds a comprehensive dashboard using SQL and Power BI.

## Dataset
[Kaggle - Supply Chain Analysis](https://www.kaggle.com/datasets/harshsingh2209/supply-chain-analysis)

## Project Steps

1. **Excel Cleaning**
   - Null values replaced with zero
   - Indexes created for `supply_id`, `order_id`
   - Data types corrected (e.g., `defect_rate`, `cost`, `revenue`) to float or int
   - Standardized date formats and categorical values
   - Added calculated fields (e.g., profits)

2. **SQL Modeling**
   - Data imported using Data Import Wizard
   - Tables created for sales, product analysis, and supplier analysis
   - ABC (product value classification) & XYZ (demand variability) analysis performed 
   - Metrics calculated: COGS, GMROI, Revenue per Product
   - Unrealistic values were updated to reflect real-world scenarios and align with the rest of the data 

3. **Power BI Dashboard**
   - Created Date-Time table, Reorder Point, and Safety Stock tables using DAX formulas
   - Sankey Charts for Supplier and Customer flow
   - Bar & Line Charts for revenue, lead time, and defect rate
   - KPI Cards for GMROI, COGS, and reorder metrics

## Key Insights

- **Top Suppliers**: Mumbai, Kolkata, Chennai
- **Reorder Point**: High for top products due to lead time and demand variance
- **Product Predictability**: High-value items show smooth supply chain performance

## Repository Structure
See folder supplychaindashboard2 breakdown for cleaned data and Power BI file.

# Supply Chain Dashboard 3 

A comprehensive supply chain analytics project using US regional sales data from Kaggle. This project includes data cleaning, SQL-based KPI analysis, and a multi-page Power BI dashboard.

## Dataset
[Kaggle - US Regional Sales Data](https://www.kaggle.com/datasets/talhabu/us-regional-sales-data)

## Project Workflow

### Step 1: Excel Cleaning
- Trimmed and re-indexed order numbers
- Transposed `sales_channel` values for relational mapping
- Corrected illogical date sequences using DAX and RAND()
- Extracted `year` and `month` from dates
- Removed currency column
- Added calculated fields: `sale_price`, `profit`, `holding_cost`
- Randomized and indexed sales team, warehouse, and product metadata
- Sales Team: Randomized names; added `sales_team_id` (1–15)
- Sale Price: `unit_price – (unit_price × discount_applied)`
- Profit: `sale_price – unit_cost`
- Holding Cost:
  - Store: Randomized between 1–10
  - Online/Wholesale/Distributor: Randomized between 5–30
- Warehouse Branch Code: Mapped to randomized location codes (e.g., `7338 → Charlotte, NC`)
- Categorical Indexing: Applied numeric IDs to `payment_type`, `customer_gender`, and other categorical fields
---

### Step 2: SQL Modeling
- Imported cleaned CSV using Data Import Wizard
- Created `Orders` table and supporting indexes
- Performed KPI analysis:
  - Sales channel profitability
  - Sales team discount vs. profit
  - EOQ, ROP, safety stock, inventory turnover
  - COGS, gross margin, time-series demand forecasting
  - ABC/XYZ classification

### Step 3: Power BI Dashboard
- Connected MySQL to Power BI
- Built 7-page dashboard:
  1. Sales Overview
  2. Sales Team Performance
  3. Inventory Metrics
  4. Product Demand
  5. Order Date Trends
  6. Financial Metrics
  7. Forecasting Insights

## Key Insights
- In-store channels have the lowest holding cost but the highest operational complexity
- Sales teams offering strategic discounts yield higher net profit
- Forecasting models show seasonal spikes in demand across product categories
- ABC/XYZ analysis reveals high-value, low-variability products ideal for automation

## Repository Structure
See folder breakdown for cleaned data and Power BI file.
