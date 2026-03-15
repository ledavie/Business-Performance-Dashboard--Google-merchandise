# Business-Performance-Dashboard--Google-merchandise


📌 Project Overview
This project transforms raw e-commerce event data from the Google Merchandise Store into a high-level executive dashboard. The goal was to provide decision-makers with a clear view of revenue drivers and identify friction points in the customer journey.

By engineering metrics from event-based logs, I moved beyond basic totals to provide deeper insights into user behavior and regional performance.

📊 Interactive Dashboard
👉 https://public.tableau.com/app/profile/lindsey.davies/viz/GoogleStoreE-CommercePerformanceDashboard/Dashboard1

🛠️ Technical Workflow
1. Data Engineering & Cleaning (Python/Pandas)
Because the raw dataset consisted of unstructured event logs, I performed extensive cleaning to make it "dashboard-ready":

Metric Engineering: Developed logic to calculate Revenue by isolating purchase events and applying price values.

Funnel Optimization: Due to the absence of session_id, I engineered User-Based Conversion metrics to track unique customer journeys.

Time-Series Prep: Standardized inconsistent date formats to allow for accurate month-over-month trend analysis.

2. Large Scale Data Handling
To maintain repository efficiency, I implemented a .gitignore strategy for the raw dataset:

Storage: The full dataset (sourced from Kaggle) is stored locally to bypass GitHub's file size limits.

Reproducibility: I have included the Python scripts used to process the data, allowing the environment to be rebuilt by placing the source CSV in the /data directory.

📊 Dashboard Features & Calculated Fields
To provide a more granular business view, I built several custom calculations in Tableau:

Cart Conversion Rate: Calculated as Total Purchases / Total Add-to-Carts to measure bottom-of-funnel efficiency.

Regional Revenue Map: A geographic breakdown of sales to identify high-growth markets.

Top 10 Product Analysis: A dynamic ranked list that filters based on category and regional selections.

💡 Key Business Insights
Conversion Bottlenecks: Analysis revealed that while specific categories like Apparel drive the highest traffic, the Office Supplies category often maintains a higher conversion-to-purchase ratio.

Regional Trends: Identified that the [Insert Region] region contributes the highest total revenue, despite having a lower average order value (AOV) compared to other regions.

📂 Repository Structure
notebooks/: Jupyter Notebooks containing data exploration and cleaning logic.

data/: Directory for source data (contains .gitignore).

visuals/: Tableau Packaged Workbook (.twbx) and static dashboard previews.

README.md: Project documentation and executive summary.
