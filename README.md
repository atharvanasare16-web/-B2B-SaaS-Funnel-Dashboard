# -B2B-SaaS-Funnel-Dashboard

# 📊 B2B SaaS Funnel Dashboard

An interactive **B2B SaaS sales funnel analytics dashboard** built with Streamlit and Plotly. Visualizes lead progression, conversion rates, revenue, and rep performance — all filterable in real time.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.57.0-red?logo=streamlit)
![Plotly](https://img.shields.io/badge/Plotly-6.x-blueviolet?logo=plotly)
![Pandas](https://img.shields.io/badge/Pandas-3.x-150458?logo=pandas)

---

## 🚀 Features

| Section | Description |
|---|---|
| **KPI Cards** | Total Leads, Closed Won, Revenue, Win Rate, Churn Rate |
| **🔻 Full Funnel** | Funnel chart showing drop-off at each stage (Lead → MQL → Demo → Trial → Won) |
| **🏢 Company Size** | Bar + line combo chart: lead volume vs. win rate by company segment |
| **⏱️ Speed to Demo** | Histogram showing how fast vs. slow MQL-to-demo booking impacts win rates |
| **📈 Monthly Trend** | Monthly lead volume bar chart with Q4 highlighted + win rate overlay |
| **🔍 Sidebar Filters** | Filter by date range, company size, and sales rep — updates all charts live |

---

## 🗂️ Project Structure

```
Python_Dashboard/
│
├── dashboard.py          # Main Streamlit dashboard app
├── quick_eda.py          # Exploratory data analysis script (run first)
├── saas_funnel_data.csv  # Synthetic B2B SaaS funnel dataset
└── README.md             # This file
```

---

## 📦 Requirements

- Python 3.10+
- streamlit
- pandas
- plotly

---

## ⚙️ Installation

**1. Clone or download this repository**

```bash
git clone https://github.com/your-username/Python_Dashboard.git
cd Python_Dashboard
```

**2. Install dependencies**

```bash
pip install streamlit pandas plotly
```

---

## ▶️ Running the App

> **Note:** If `streamlit` is not in your system PATH (common on Windows), use the `python -m` approach below.

```bash
python -m streamlit run dashboard.py
```

Then open your browser at **http://localhost:8501**

---

## 🔍 Exploratory Data Analysis (Optional)

Before launching the dashboard, you can run the EDA script to inspect the raw dataset in the terminal:

```bash
python quick_eda.py
```

This prints:
- Dataset shape and sample rows
- Column types and missing value counts
- Funnel stage drop-off percentages
- Lead source breakdown and cross-tab
- Revenue stats (total, average, median, max deal size)
- Speed-to-demo statistics
- Sales rep lead distribution

---

## 📊 Dataset — `saas_funnel_data.csv`

Synthetic dataset representing a B2B SaaS sales funnel. Key columns:

| Column | Description |
|---|---|
| `lead_id` | Unique lead identifier |
| `created_date` | Date the lead entered the funnel |
| `company_size` | Startup / SMB / Mid-Market / Enterprise |
| `lead_source` | Where the lead came from |
| `sales_rep` | Assigned sales representative |
| `current_stage` | Current funnel stage or final outcome |
| `deal_value` | Revenue value (for closed deals) |
| `mql_date` | Date lead became Marketing Qualified |
| `demo_booked_date` | Date demo was scheduled |
| `demo_completed_date` | Date demo took place |
| `trial_start_date` | Date free trial began |
| `closed_date` | Date deal was closed |
| `days_mql_to_demo_booked` | Days elapsed from MQL to demo booking |

---

## 🛠️ Tech Stack

- **[Streamlit](https://streamlit.io/)** — Web app framework for Python data apps
- **[Plotly](https://plotly.com/python/)** — Interactive charts (Funnel, Bar, Scatter, Histogram)
- **[Pandas](https://pandas.pydata.org/)** — Data loading, filtering, and aggregation

---

## 📝 Notes

- All data in `saas_funnel_data.csv` is **synthetic** (generated for demo purposes).
- The `use_container_width` deprecation warnings from Streamlit are harmless — will be updated in a future version.

---

*Built with Streamlit + Plotly · Data is synthetic · @loresowhat*
