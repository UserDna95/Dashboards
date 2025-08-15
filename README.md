# Dashboards
Compilation of various dashboards on Power BI and Tableau

# Supply Chain Dashboard 1

## Problem Statement
How did service levels affect contract renewal for customers?
This project analyzes key supply chain metrics to understand their impact on customer retention and contract renewals. Built using Excel for data cleaning and Power BI for visualization.

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
- OTIF and On-Time metrics significantly below target
- Potential causes: poor route optimization, inventory issues, production delays

## Recommendations
- Improve route optimization and vendor selection
- Enhance inventory and production efficiency
- Strengthen vendor relationships
- Investigate reasons for contract discontinuation (pricing, service, logistics)

## How to Use
1. Open `dashboard.pbix` in Power BI
2. Review `data_model_overview.md` for structure
3. Explore insights in `service_level_analysis.md`
