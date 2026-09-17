# E-commerce-analysis-

# 📊 E-Commerce Sales Analytics Dashboard

A complete, end-to-end data analyst portfolio project: synthetic data generation,
SQL analysis, exploratory data analysis in Python, and an interactive Streamlit
dashboard — all in one repo.

## 🔍 Overview

This project analyzes e-commerce transaction data (2024–2025) to surface insights on:

- Revenue trends over time (seasonality, festive-season spikes)
- Best-performing product categories and products
- Regional / city-level sales performance
- Customer segment behavior (New / Returning / VIP)
- Payment method preferences
- Order return & cancellation rates

## 🗂️ Project Structure

```
ecommerce-analytics-dashboard/
├── data/
│   ├── generate_data.py       # Generates the synthetic dataset
│   └── ecommerce_data.csv     # 6,000-row transactions dataset
├── notebooks/
│   ├── analysis.ipynb         # Full EDA notebook (charts + insights)
│   └── analysis.py            # Same analysis as a standalone script
├── sql/
│   └── analysis_queries.sql   # 10 SQL queries (revenue, RFM, returns, etc.)
├── dashboard/
│   └── app.py                 # Interactive Streamlit dashboard
├── images/                    # Exported chart PNGs (from analysis.py)
├── requirements.txt
├── LICENSE
└── README.md
```

## 📦 Dataset

`data/ecommerce_data.csv` contains 6,000 synthetic orders with the following fields:

| Column | Description |
|---|---|
| `order_id` | Unique order identifier |
| `order_date` | Date of order |
| `customer_id` | Unique customer identifier |
| `customer_segment` | New / Returning / VIP |
| `region`, `city` | Delivery location |
| `category`, `product` | Product details |
| `unit_price`, `quantity` | Pricing |
| `gross_amount`, `discount_pct`, `discount_amount`, `net_amount` | Order value breakdown |
| `payment_method` | Credit Card / Debit Card / UPI / Net Banking / COD |
| `order_status` | Completed / Returned / Cancelled |
| `rating` | Customer rating (1–5, completed orders only) |

Regenerate it anytime with:

```bash
python data/generate_data.py
```

## 🚀 Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/akash-m06/ecommerce-analytics-dashboard.git
cd ecommerce-analytics-dashboard

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the EDA script (regenerates chart images)
python notebooks/analysis.py

# 4. Launch the interactive dashboard
streamlit run dashboard/app.py
```

Or open `notebooks/analysis.ipynb` directly in Jupyter / VS Code / Google Colab.

## 📈 Sample Insights

- Revenue peaks noticeably in **October–November**, driven by festive-season discounting.
- **Electronics** and **Fashion** are the top two revenue-generating categories.
- **VIP** customers make up the smallest segment but have the highest average order value.
- **UPI** and **Credit Card** are the most-used payment methods.
- Overall return + cancellation rate is around **7%**, varying by category.

## 🖥️ Interactive Dashboard

The Streamlit dashboard (`dashboard/app.py`) lets you filter by date range, region,
category, customer segment, and order status, with live-updating KPIs and charts
for revenue trend, category/product performance, regional breakdown, customer
segment share, and payment methods.

## 🛠️ Tech Stack

- **Python**: pandas, numpy for data processing
- **Visualization**: matplotlib, seaborn (static), Plotly (interactive)
- **Dashboard**: Streamlit
- **SQL**: Analysis queries compatible with SQLite/PostgreSQL/MySQL


## 👤 Author

**Akash** — CS undergraduate | Developer & Designer
[GitHub](https://github.com/akash-m06) · [LinkedIn](https://linkedin.com/in/ananthakash-m)
