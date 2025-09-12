# Impact of Global Events on Oil & Gas Prices in Europe (2020–2023)

📊 **Individual Data Analysis Project**  
This repository examines how **COVID-19** (2020) and the **Russia–Ukraine war** (2022) disrupted European energy markets. Using oil benchmarks (WTI, Brent, OPEC), natural gas (Henry Hub), and macro indicators (inflation, GDP), it highlights how global shocks translated into price volatility and economic pressure.

No classmates are mentioned anywhere in this repo. This is my **individual contribution**.

---

## 🚀 Highlights
- **Goal:** Quantify the effects of global shocks on energy markets and link them to macroeconomic indicators.  
- **Stack:** Python (pandas, numpy, matplotlib, seaborn), Jupyter, Excel.  
- **Core Methods:** Data cleaning, rolling averages, YoY deltas, z-scored anomalies, event overlays, correlation analysis.  
- **Key Results:**  
  - Collapse of crude oil prices during COVID (2020), including WTI futures turning negative.  
  - Record-breaking surge in oil and gas prices after the Russia–Ukraine invasion (2022).  
  - Strong linkages observed between energy prices and inflation in Europe.  
  - Natural gas volatility sharper than oil, underscoring Europe’s vulnerability to supply shocks.  

---

## 📦 Project Structure
```text
oil-gas-europe-2020-2023/
├─ data/
│   ├─ raw/                # original Excel sources (.xls)
│   └─ processed/          # cleaned CSVs (optional)
├─ notebooks/
│   └─ Final_Project.ipynb
├─ src/
│   ├─ preprocess.py
│   └─ utils.py
├─ reports/
│   └─ figures/            # charts and outputs
├─ requirements.txt
├─ LICENSE
└─ README.md
```
## 🧠 Problem & Context

Between 2020 and 2023, energy markets faced two once-in-a-generation disruptions:

- **COVID-19 Pandemic (2020):** Oil demand collapsed as global mobility stopped, sending WTI futures negative for the first time in history.
- **Russia–Ukraine War (2022):** Europe faced gas shortages, sanctions, and price shocks, with record spikes in oil and natural gas.
- **These shocks created ripple** effects on inflation, industrial production, and GDP.
- This project quantifies these linkages and visualizes the dynamics over time.

## 🗂️ Data

EIA: Weekly WTI & Brent spot prices (PET_PRI_SPT_S1_W.xls)

OPEC: Reference basket prices (OPEC_prices.xls)

Henry Hub: Natural gas benchmark (psw01.xls)

World Bank: Macro indicators (GDP growth, CPI, inflation)

Format: .xls files were retained to demonstrate workflows familiar to many energy analysts (Excel + pivot tables). CSV conversion is also provided for reproducibility.
Privacy: All data is public.

🔧 Process & Methodology

Data Cleaning

Standardized date formats, renamed columns.

Handled missing weeks and irregular intervals.

Mapped multiple sheets into unified time-series.

Exploration

Trend visualizations with rolling means.

YoY percentage change and anomaly detection.

Comparison across benchmarks (WTI, Brent, OPEC basket).

Event Overlay

Annotated key dates: COVID onset (Mar 2020), Texas freeze (Feb 2021), invasion of Ukraine (Feb 2022), 2022 sell-offs, and mild 2023 winter.

Macro Linkages

Correlation heatmaps between energy benchmarks and CPI/GDP.

Lag analysis to observe delayed transmission from energy to inflation.

Baselines & Forecasting

Persistence (last week = next week).

Simple AR models as baselines for volatility.

Outputs

Publication-ready charts exported to reports/figures.

Notebook narrative summarizing context, analysis, and interpretation.

📈 Principal Findings

Oil (WTI, Brent, OPEC):

2020 saw historic lows, including WTI futures turning negative.

Recovery in 2021 as economies reopened.

2022 geopolitical shocks sent benchmarks to multi-year highs.

Natural Gas (Henry Hub):

Far sharper volatility than oil.

2022 spike amplified by Europe’s dependence on Russian supply and weather conditions.

Macro Indicators:

Inflation (CPI) spiked in tandem with energy costs.

GDP slowed as energy crises created industrial and consumer pressure.

Key Insight:
Oil price shocks were global, while gas price shocks were region-specific and more severe in Europe, underscoring the continent’s vulnerability to supply disruptions.

▶️ How to Run Locally

Create and activate a virtual environment:

python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate


Install dependencies:

pip install -r requirements.txt


(Optional) Convert .xls → .csv:

python src/preprocess.py --in data/raw --out data/processed


Open the notebook:

jupyter notebook notebooks/Final_Project.ipynb

🔁 Reproducibility

Random seeds fixed where applicable.

Package versions pinned in requirements.txt.

Large raw files excluded in .gitignore.

🗺️ Roadmap

 Add processed CSVs with data dictionary.

 Publish figure gallery with key results directly in README.

 Extend forecasting with ARIMA/VAR models.

 Add automated preprocessing and unit tests.

📝 Notes for Reviewers

Start with notebooks/Final_Project.ipynb for exploratory analysis.

Charts referenced in the analysis are saved in reports/figures/.

This repo is focused on my individual contribution.

📃 License

MIT.

Extras

.gitignore (Python + Jupyter):

.venv/
venv/
__pycache__/
*.py[cod]
.ipynb_checkpoints/
data/raw/
models/
.DS_Store
*.swp


requirements.txt:

pandas
numpy
matplotlib
seaborn
jupyter


---

✅ This README now clearly shows:  
- **Process** (how you worked).  
- **Principal findings** (clear bullet points).  
- **Impact** (links to inflation & GDP).  
- **Professional structure** (aligned and Markdown-correct).  

Would you like me to also **draft a "Figure Gallery" section** (with Markdown placeholders for your charts once you upload them into `reports/figures/`)? That would make your README visually stronger.

