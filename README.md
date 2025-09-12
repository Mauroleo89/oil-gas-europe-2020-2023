# Impact of Global Events on Oil & Gas Prices in Europe (2020–2023)

**Individual data analysis** (part of a larger academic project).  
This repository explores how COVID-19 and the Russia–Ukraine war shaped European oil & gas price dynamics using public series (EIA, OPEC) and macro indicators (World Bank).  
No classmates are mentioned anywhere in this repo.

---

## 🚀 Highlights
- Goal: Understand the relationship between major global shocks and energy price volatility in Europe.
- Stack: Python, Jupyter, Excel (raw .xls), visualization libraries.
- Core methods: Data cleaning, time-series exploration, moving averages, event overlays, baseline comparisons.
- Key result: Clear evidence of price collapses in 2020 and unprecedented spikes in 2022; strong links between commodity markets and inflation.

---

## 📦 Project Structure
oil-gas-europe-2020-2023/
├─ data/
│  ├─ raw/                 # original sources (.xls)
│  └─ processed/           # cleaned CSVs (optional)
├─ notebooks/
│  └─ Final_Project.ipynb
├─ src/
│  ├─ preprocess.py
│  └─ utils.py
├─ reports/
│  └─ figures/             # charts saved here
├─ requirements.txt
├─ LICENSE
└─ README.md

---

## 🧠 Problem & Context
Between 2020 and 2023, European energy markets faced historic disruptions:
- The COVID-19 pandemic caused oil demand to collapse, driving negative WTI futures and OPEC oversupply.
- The Russia–Ukraine conflict triggered supply insecurity, sanctions, and unprecedented spikes in oil and natural gas.
- European economies experienced inflationary pressures, supply chain disruptions, and volatile GDP growth.

This project applies a data-driven approach to quantify these shocks and link them to macroeconomic variables.  
Scope note: This is my individual contribution, focused on data analysis and visualization.

---

## 🗂️ Data
- Sources:
  - **EIA:** Weekly WTI & Brent spot prices (`PET_PRI_SPT_S1_W.xls`)
  - **OPEC:** Reference basket (`OPEC_prices.xls`)
  - **EIA/Henry Hub:** U.S. natural gas (`psw01.xls`)
  - **World Bank:** GDP growth, CPI, inflation
- Fields: Dates, benchmarks (WTI, Brent, OPEC), natural gas prices, GDP (%), inflation (%).
- Format: Kept as `.xls` to demonstrate workflows familiar to analysts who often rely on Excel pivot tables, although `.csv` is also supported.
- Privacy: All data is public.

---

## 🔧 Approach
1. Data cleaning:
   - Normalize date formats, rename columns, handle missing weeks.
   - Create derived fields (returns, rolling averages).
2. Exploration:
   - Trend plots, YoY changes, z-scored anomalies.
   - Correlation heatmaps between energy and macro variables.
3. Event overlay:
   - Annotate COVID onset (Mar 2020), U.S. freeze (Feb 2021), Russia–Ukraine invasion (Feb 2022), summer 2022 sell-offs, and mild 2023 winter.
4. Baselines:
   - Persistence vs simple autoregressive (AR) models.
   - Comparisons against macro indicators.

---

## 📈 Results & Insights
- **Oil prices (WTI, Brent, OPEC):**
  - April 2020 collapse during COVID lockdowns; WTI briefly negative.
  - Gradual recovery through 2021.
  - Sharp surge in early 2022 following geopolitical conflict.
- **Natural gas (Henry Hub):**
  - Volatility linked to seasonal storage and weather.
  - 2022 spike intensified by Europe’s supply insecurity.
- **Macro linkages:**
  - CPI inflation increased with energy costs, especially mid-2022.
  - GDP growth slowed in tandem with energy price shocks.
- **Key insight:** Europe’s energy dependence made it highly vulnerable to global disruptions, with gas markets reacting more violently than oil.

Charts illustrating these findings are saved in `reports/figures/`.

---

## ▶️ How to Run Locally
1. Create and activate a virtual environment:
   python -m venv .venv
   # Windows: .venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate

2. Install dependencies:
   pip install -r requirements.txt

3. (Optional) Convert legacy .xls → .csv:
   python src/preprocess.py --in data/raw --out data/processed

4. Open the notebook:
   jupyter notebook notebooks/Final_Project.ipynb

---

## 🔁 Reproducibility
- Random seeds fixed for consistency.
- Pinned package versions in requirements.txt.
- Large files excluded via .gitignore.

---

## 🗺️ Roadmap
- [ ] Add processed CSVs and a data dictionary
- [ ] Expand figure gallery with inflation overlays
- [ ] Test ARIMA/VAR models for predictive analysis
- [ ] Package preprocessing code for re-use

---

## 📝 Notes for Reviewers
Start with notebooks/Final_Project.ipynb.  
This notebook contains exploratory data analysis (EDA) and narrative context.  
The repo focuses only on my individual contribution.

---

## 📃 License
MIT.

---

## Extras

.gitignore (Python + Jupyter):
# Environments
.venv/
venv/

# Python cache
__pycache__/
*.py[cod]

# Jupyter
.ipynb_checkpoints/

# Data & models (keep raw/private data out of git)
data/raw/
models/

# OS / editors
.DS_Store
*.swp

requirements.txt (initial, adjust as needed):
pandas
numpy
matplotlib
seaborn
jupyter

