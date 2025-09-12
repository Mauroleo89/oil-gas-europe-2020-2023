# Impact of Global Events on Oil & Gas Prices in Europe (2020–2023)

**Individual data analysis** (part of a larger academic project).  
This repository explores how **COVID-19** and the **Russia–Ukraine war** shaped European oil & gas price dynamics using public series (EIA, OPEC) and macro indicators (World Bank).  
_No classmates are mentioned anywhere in this repo._

---

## 🚀 Highlights
- **Goal:** Analyze how global shocks affected oil & gas price dynamics in Europe.  
- **Stack:** Python, Jupyter, Excel.  
- **Core methods:** Data cleaning, time-series visualization, simple AR models.  
- **Key result:** Strong correlations between global events and price volatility.

---

## 📦 Project Structure
```text
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
🧠 Problem & Context
Energy prices in Europe whipsawed between 2020 and 2023.
This project analyzes how two shocks—COVID-19 (2020) and the Russia–Ukraine war (2022)—propagated into oil (WTI/Brent), gas (Henry Hub), and macro indicators (inflation, GDP).

Scope note: This is my individual contribution focused on data analysis. It distills, cleans, and visualizes public data; it does not include team content or classmates’ names.

🗂️ Data
Sources (raw):

EIA weekly spot prices (PET_PRI_SPT_S1_W.xls)

OPEC reference prices (OPEC_prices.xls)

Henry Hub & production (psw01.xls)

World Bank macro indicators

Fields (typical): Date, WTI, Brent, OPEC basket, natural gas (USD/MMBtu), GDP growth, CPI.

Privacy: All data is public.

ℹ️ I decided to keep the raw .xls format in this repo to demonstrate workflows familiar to many energy analysts (who often use pivot tables in Excel). Good practice would be to convert to .csv, but here I show both approaches.

🔧 Approach
Cleaning: harmonize dates, rename columns, handle missing weeks.

Exploration: rolling means, YoY deltas, correlation heatmaps.

Events overlay: COVID onset, 2021 US freeze, 2022 invasion, 2022 sell-offs, 2023 mild winter.

Baselines: naive persistence vs simple AR models.

Outputs: publication-ready charts in reports/figures/.

📈 Results
Observed: strong price spikes around early 2022; elevated volatility.

Interpretation: shocks transmit to CPI/GDP with a lag.

Limitations: correlation ≠ causation; macro series differ in frequency/revisions.

▶️ How to Run Locally
Create and activate a virtual environment:

bash
Copy code
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
Install dependencies:

bash
Copy code
pip install -r requirements.txt
(Optional) Convert legacy .xls → .csv:

bash
Copy code
python src/preprocess.py --in data/raw --out data/processed
Open the notebook:

bash
Copy code
jupyter notebook notebooks/Final_Project.ipynb
🔁 Reproducibility
Fixed seeds for any random steps.

Pinned versions in requirements.txt.

Large files kept out of Git (see .gitignore).

🗺️ Roadmap
 Add processed CSVs with a data dictionary

 Publish figure gallery in README

 Optional: add ARIMA baseline for WTI/Brent

 Add unit tests for loaders

📝 Notes for Reviewers
Start with notebooks/Final_Project.ipynb for EDA.
The academic background is summarized here as an individual contribution.

📃 License
MIT.

Extras
.gitignore (Python + Jupyter):

gitignore
Copy code
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

text
Copy code
pandas
numpy
matplotlib
seaborn
jupyter
yaml
Copy code

---

👉 This way, it’s **one block** to copy-paste into your README.md.  
Do you want me to also prepare a **shorter “executive summary” version** (1–2 paragraphs) for LinkedIn o
