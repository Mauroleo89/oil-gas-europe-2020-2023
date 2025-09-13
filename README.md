# Impact of Global Events on Oil & Gas Prices in Europe (2020–2023)

📊 **Individual Data Analysis Project**  
This repository examines how **COVID-19** (2020) and the **Russia–Ukraine war** (2022) disrupted European energy markets. Using oil benchmarks (WTI, Brent, OPEC), natural gas (Henry Hub), and macro indicators (inflation, GDP), it highlights how global shocks translated into price volatility and economic pressure. No classmates are mentioned anywhere in this repo. This is my **individual contribution**.

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

---

## 📊 Data
- **EIA:** Weekly WTI & Brent spot prices (`PET_PRI_SPT_S1_W.xls`)  
- **OPEC:** Reference basket prices (`OPEC_prices.xls`)  
- **Henry Hub:** Natural gas benchmark (`psw01.xls`)  
- **World Bank:** Macro indicators (GDP growth, CPI, inflation)  

Format: `.xls` files were retained to demonstrate workflows familiar to many energy analysts (Excel + pivot tables). CSV conversion is also provided for reproducibility.  
Privacy: All data is public.

---

## 🔧 Process & Methodology
1. **Data Cleaning**  
   - Standardized date formats and renamed columns.  
   - Handled missing weeks and irregular intervals.  
   - Mapped multiple Excel sheets into unified time-series datasets.  

2. **Exploration**  
   - Trend visualizations with rolling averages.  
   - Year-over-year percentage changes and anomaly detection.  
   - Comparison across benchmarks (WTI, Brent, OPEC basket).  

3. **Event Overlay**  
   - Annotated key dates:  
     - COVID onset (Mar 2020)  
     - Texas freeze (Feb 2021)  
     - Russia–Ukraine invasion (Feb 2022)  
     - 2022 summer sell-offs  
     - Mild winter in early 2023  

4. **Macro Linkages**  
   - Correlation heatmaps between energy benchmarks and CPI/GDP.  
   - Lag analysis to observe delayed transmission from energy prices to inflation.  

5. **Baselines & Forecasting**  
   - Naive persistence models (last week = next week).  
   - Simple AR models for volatility context.  

6. **Outputs**  
   - Publication-ready charts in `reports/figures`.  
   - A notebook narrative summarizing process, analysis, and interpretation.  

---

## 📈 Principal Findings
- **Oil (WTI, Brent, OPEC):**  
  - 2020 saw historic lows, including WTI futures turning negative.  
  - Recovery through 2021 with economic reopening.  
  - 2022 geopolitical shocks sent benchmarks to multi-year highs.

<img width="847" height="725" alt="Crude_price" src="https://github.com/user-attachments/assets/43e22c70-5f76-412a-bbdc-1ab9949ea437" />

<img width="1001" height="624" alt="Produ_oil" src="https://github.com/user-attachments/assets/a6817a67-743f-4a06-8457-d4866000c5bf" />

- **Natural Gas (Henry Hub):**  
  - Higher volatility than oil, driven by seasonal storage and weather.  
  - 2022 spike amplified by Europe’s reliance on Russian supply.  

- **Macro Indicators:**  
  - CPI inflation spiked in parallel with energy costs, peaking mid-2022.  
  - GDP growth slowed as energy crises created industrial and consumer strain.
 
- **Key Insight:**  
  Oil shocks were **global**, while gas shocks were **region-specific** and more severe in Europe, highlighting the continent’s vulnerability to supply disruptions.

  
<img width="806" height="689" alt="Corr_matrix" src="https://github.com/user-attachments/assets/b8c4b8ae-b18b-48fa-afb0-7b6e8ddfcc74" />

---

## ▶️ How to Run Locally
1. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   # Windows: .venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate

2. Install dependencies:
   ```bash
   pip install -r requirements.txt

## 🗺️ Roadmap

- Add processed CSVs with data dictionary.
- Publish figure gallery with key results directly in README.
- Extend forecasting with ARIMA/VAR models.
-  Add automated preprocessing and unit tests.

## 📝 Notes for Reviewers

- Start with notebooks/Final_Project.ipynb for the exploratory analysis.
- Figures summarizing results are stored in reports/figures/.
- This repo focuses exclusively on my individual analysis contribution.
