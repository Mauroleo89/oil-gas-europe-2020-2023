# Impact of Global Events on Oil & Gas Prices in Europe (2020–2023)

**Individual data analysis** (part of a larger academic project). This repository explores how COVID‑19 and the Russia–Ukraine war shaped European oil & gas price dynamics using public series (EIA, OPEC) and macro indicators (World Bank). No classmates are mentioned anywhere in this repo.

---

## 🚀 Highlights

* **Goal:** \<What problem are you solving?>
* **Stack:** \<Python / Jupyter / SQL / etc.>
* **Core methods:** \<e.g., feature engineering, linear regression, random forest>
* **Key result:** \<RMSE / accuracy / business impact / visualization>

---

## 📦 Project Structure

````text
oil-gas-europe-2020-2023/
├─ data/
│  ├─ raw/                 # original sources (.xls kept out of Git LFS if large)
│  └─ processed/           # cleaned CSVs
├─ notebooks/
│  ├─ 01_explore.ipynb
│  └─ 02_modeling.ipynb
├─ src/
│  ├─ preprocess.py
│  └─ utils.py
├─ reports/
│  └─ figures/             # charts saved here and embedded in README
├─ requirements.txt
├─ LICENSE
├─ README.md
└─ .gitignore
```text
project-name/
├─ data/                # sample or synthetic data only (no private data)
├─ notebooks/           # exploratory & training notebooks
├─ src/                 # reusable Python code
├─ reports/             # figures and final outputs
├─ requirements.txt     # dependencies
├─ README.md            # this file
└─ .gitignore           # ignore venv, data/raw, checkpoints
````

> If your current files are different, we’ll map them into this structure.

---

## 🧠 Problem & Context

Energy prices in Europe whipsawed between 2020 and 2023. This project analyzes how two shocks—**COVID‑19 (2020)** and the **Russia–Ukraine war (2022)**—propagated into oil (WTI/Brent), gas (Henry Hub) and macro indicators (inflation, GDP) using time‑series exploration and simple baselines.

**Scope note:** This is my **individual contribution** focused on data analysis. It distills, cleans, and visualizes public data; it does **not** include team content or classmates’ names.

---

## 🗂️ Data

* **Sources (raw)**: EIA weekly spot prices (`PET_PRI_SPT_S1_W.xls`), OPEC price series (`OPEC_prices.xls`), Henry Hub & production (`psw01.xls`), macro indicators (World Bank). Raw .xls files are stored under `data/raw/` and converted to CSV in `data/processed/` for reproducibility.
* **Fields (typical)**: Date, commodity benchmark (WTI, Brent, OPEC), price (USD/bbl), natural gas price (USD/MMBtu), GDP growth (%, annual), CPI/inflation (%, YoY).
* **Privacy**: All data is public. No personal or institutional confidential data.

> Tip: Convert legacy `.xls` to `.csv` before analysis for easier GitHub preview and diffs.

---

## 🔧 Approach

* **Cleaning**: harmonize dates, rename columns, handle missing weeks, convert `.xls` → `.csv`.
* **Exploration**: rolling means, YoY deltas, z‑scored anomalies; correlation heatmaps (macro vs energy).
* **Events overlay**: annotate 2020‑03 (COVID onset), 2021‑02 (US freeze), 2022‑02‑24 (RU–UA invasion), 2022‑06/09 (sell‑offs), 2023 mild winter.
* **Baselines**: naive persistence vs simple AR models (optional) to contextualize volatility.
* **Outputs**: publication‑ready charts in `reports/figures/`.

---

## 📈 Results

* **Observed**: strong price spikes around early 2022 and elevated volatility; macro linkages visible in correlations. See `reports/figures/`.
* **Interpretation**: shocks transmit to CPI/GDP with a lag; Europe mirrors global crude benchmarks while gas shows weather‑ and storage‑driven swings.
* **Limitations**: correlations are not causation; macro series differ in frequency and revisions.

---

## ▶️ How to Run Locally

1. Create and activate a virtual environment

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Prepare data (convert legacy .xls → .csv)

```bash
python src/preprocess.py --in data/raw --out data/processed
```

4. Open the notebooks

```bash
jupyter notebook notebooks/01_explore.ipynb
```

---

## 🔁 Reproducibility

* Fixed seeds for any random steps.
* Pinned versions in `requirements.txt`.
* Large artifacts kept out of Git (see `.gitignore`).

---

## 🗺️ Roadmap

* [ ] Add processed CSVs with a data dictionary
* [ ] Publish figure gallery in README
* [ ] Optional: simple ARIMA baseline for WTI/Brent
* [ ] Add unit tests for loaders

---

## 📝 Notes for Reviewers

Start with `notebooks/01_explore.ipynb` for EDA. The academic background of the analysis and key narratives are summarized here (individual contribution), without referencing classmates. A related write‑up exists but is not included to keep this repo focused on code and data.

---

## 📃 License

MIT.

---

### Extras

**.gitignore (Python + Jupyter):**

```gitignore
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
```

**requirements.txt (initial, adjust as needed):**

```text
pandas
numpy
matplotlib
seaborn
jupyter
```

> Current notebook imports detected: pandas, numpy, matplotlib, seaborn. Add others if you use them (e.g., statsmodels, scipy).

