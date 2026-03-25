📊 Banking Campaign Analytics & Segmentation Platform

End-to-end data analytics project simulating a real-world banking campaign system — from raw data generation to customer segmentation and executive dashboards.


🏦 Project Overview
This project replicates the work of a Data Analyst at a retail bank, covering the full analytics lifecycle:

Simulating realistic banking campaign data (1,000 customers, 5 campaigns, 5,000 responses)
Building an ETL pipeline to load data into PostgreSQL
Performing RFM-based customer segmentation using K-Means clustering
Delivering interactive Power BI dashboards tracking campaign KPIs

Key Finding: Targeted campaigns (matched to customer income segment) achieved a 35% conversion rate vs only 8% for mismatched campaigns — a 4x difference in effectiveness.

🛠️ Tech Stack
LayerToolData GenerationPython (pandas, numpy, faker)DatabasePostgreSQLSegmentationPython (scikit-learn, K-Means)DashboardPower BIVersion ControlGit & GitHub

📁 Project Structure
campaign_project/
│
├── data/
│   ├── raw/                  # Generated CSV files
│   │   ├── customers.csv
│   │   ├── campaigns.csv
│   │   └── responses.csv
│   └── processed/            # Cleaned & transformed data
│
├── notebooks/
│   ├── 01_data_generation.ipynb    # Phase 1: Simulate banking data
│   ├── 02_etl_pipeline.ipynb       # Phase 2: Extract, Transform, Load
│   └── 03_segmentation.ipynb       # Phase 3: RFM + K-Means clustering
│
├── dashboard/
│   └── campaign_analytics.pbix     # Power BI dashboard
│
├── screenshots/
│   ├── dashboard_overview.png
│
└── README.md

🔄 How It Works
Phase 1 — Data Generation
Simulated realistic Indian banking data using Python's faker library with intentional patterns:

1,000 customers across 8 cities with correlated income and balance
5 campaigns targeting different income segments (Low / Medium / High / Premium)
5,000 campaign responses with realistic conversion logic — matched campaigns convert at 35%, mismatched at 8%

Phase 2 — ETL Pipeline

Extracted raw CSVs and validated data quality
Transformed data using pandas (type casting, merging, feature engineering)
Loaded clean data into PostgreSQL for structured querying

Phase 3 — Customer Segmentation
Applied RFM Analysis (Recency, Frequency, Monetary) combined with K-Means clustering to segment customers into groups:
SegmentDescriptionChampionsHigh balance, frequent responders, recent activityLoyal CustomersRegular engagement, medium balanceAt RiskPreviously active, recently dropped offDormantLow engagement, low balance
Phase 4 — Dashboard & Insights
Built an interactive Power BI dashboard answering key business questions:

Which campaign had the highest conversion rate?
Which channel (Email / SMS / App) performed best?
Which cities hold the most customer value?
How do customer segments differ in response behaviour?


💡 Key Insights

Segment matching drives 4x higher conversion — campaigns targeted at the right income group convert at 35% vs 8%
Email dominates as the highest performing channel at ~40% of total responses
Premium segment generates disproportionate balance value despite smaller customer count
Mumbai and Chennai lead in total customer balance across all cities


🚀 How to Run
1. Clone the repo
bashgit clone https://github.com/rashisureka/camapaign-analytics.git
cd camapaign-analytics
2. Install dependencies
bashpip install pandas numpy faker scikit-learn matplotlib seaborn sqlalchemy psycopg2-binary
3. Run notebooks in order

01_data_generation.ipynb → generates CSVs in data/raw/
02_etl_pipeline.ipynb → loads data into PostgreSQL
03_segmentation.ipynb → runs RFM + K-Means segmentation

4. Open dashboard

Open dashboard/campaign_analytics.pbix in Power BI Desktop
