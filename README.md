# 📊 AI Business Insight Generator

An AI-powered business intelligence dashboard built with **Streamlit**, **Plotly**, and **Google Gemini**. Upload any business/sales CSV dataset (e.g. Superstore data) and instantly get interactive KPI dashboards, visual analytics, and AI-generated business insights — complete with an executive summary, risks, opportunities, recommendations, and a computed business health score.

## 🚀 Live Demo

[View Deployed App on Streamlit Cloud](https://nikitadokrimare-da-21-business-insights-dashboard-app-kosxyq.streamlit.app/)

## ✨ Features

- **📄 CSV Upload** — Upload any business dataset in CSV format (with automatic encoding fallback).
- **📈 KPI Dashboard** — Auto-calculated metrics: Total Sales, Total Profit, Orders, Customers, and Average Discount.
- **📊 Interactive Visualizations** — Sales by Category, Profit by Region, and Sales by Segment charts powered by Plotly.
- **🤖 AI-Powered Insights (RAG)** — Ask natural language business questions (e.g. *"Why did sales drop last month?"*) and get AI-generated answers using Google Gemini, grounded in your data's KPI summary and custom business rules.
- **⭐ Business Health Score** — An automatically calculated score (0–100) with a status rating (Excellent / Good / Average / Critical).
- **📌 Quick Summary Cards** — Instantly see the top/lowest performing category and best/worst performing region.
- **⬇️ Downloadable Reports** — Export a plain-text AI business insight report.

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Frontend / App Framework | [Streamlit](https://streamlit.io/) |
| Data Handling | [Pandas](https://pandas.pydata.org/) |
| Visualizations | [Plotly Express](https://plotly.com/python/plotly-express/) |
| AI / LLM | [Google Gemini](https://ai.google.dev/) (`google-generativeai`) |
| Config / Secrets | [python-dotenv](https://pypi.org/project/python-dotenv/) |

## 📁 Project Structure

```
Business-Insights-Dashboard/
├── app.py                 # Main Streamlit application
├── gemini_models.py        # Gemini model helper/config
├── testgemini.py           # Script to test Gemini API connectivity
├── Superstoredata.csv       # Sample business dataset
├── requirements.txt         # Python dependencies
├── knowledge/
│   └── business_rules.txt   # Custom business rules used for AI context (RAG)
└── .gitignore
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/NikitaDokrimare-DA-21/Business-Insights-Dashboard.git
cd Business-Insights-Dashboard
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source  venv\Scripts\activate     
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up your Gemini API Key

Create a `.env` file in the project root and add your [Google Gemini API key](https://ai.google.dev/):

```
GEMINI_API_KEY=your_api_key_here
```

### 5. Run the app

```bash
streamlit run app.py
```

The dashboard will open in your browser at `http://localhost:8501`.

## 📖 Usage

1. Launch the app and upload a business CSV dataset (must include columns like `Sales`, `Profit`, `Order ID`, `Customer ID`, `Discount`, `Category`, `Region`, `Segment` — a sample `Superstoredata.csv` is included).
2. Review the auto-generated KPI cards and charts.
3. Type a business question in the **"Ask Your Business Question"** box (e.g. *"What can we do to improve profit in the worst-performing region?"*).
4. Click **🚀 Generate AI Insights** to get a full AI-generated report with an executive summary, key insights, risks, opportunities, recommendations, and a business health score.
5. Download the generated report for offline use.

## 📋 Requirements

- Python 3.9+
- A valid Google Gemini API key

See `requirements.txt` for the full list of Python packages:

```
streamlit
pandas
plotly
google-generativeai
python-dotenv
```

## 🔒 Notes

- Your `GEMINI_API_KEY` should **never** be committed to the repository — keep it in a local `.env` file, which is excluded via `.gitignore`.
- The dashboard expects specific column names (`Sales`, `Profit`, `Order ID`, `Customer ID`, `Discount`, `Category`, `Region`, `Segment`). Adjust `app.py` if your dataset uses different column names.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/NikitaDokrimare-DA-21/Business-Insights-Dashboard/issues).


## 👤 Author

**Nikita Dokrimare**
[GitHub Profile](https://github.com/NikitaDokrimare-DA-21)
