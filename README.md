# Trader Behavior vs Market Sentiment (Primetrade.ai Assignment)

## 📌 Overview
This project explores how trader behavior (profitability, risk, and volume) aligns or diverges from Bitcoin market sentiment (Fear vs Greed).

**Datasets**
- **Hyperliquid Trader Data**: account, side, size (USD/tokens), execution price, PnL, timestamps.
- **Fear & Greed Index**: daily Bitcoin market sentiment.

> ⚠️ **Note:** The provided datasets do not overlap in time. This repo demonstrates the framework and methodology. On overlapping data, the same pipeline would produce sentiment-aligned insights.

---

## 📂 Project Structure
```
ds_aaysha_sheikh/
├── notebook_1.ipynb # Data preparation & cleaning
├── notebook_2.ipynb # Analysis, plots, and stats tests
├── csv_files/ # Cleaned data & analysis tables
│ ├── hyperliquid_trades_clean.csv
│ ├── fear_greed_clean.csv
│ ├── trades_with_sentiment.csv
│ ├── daily_sentiment_summary.csv
│ ├── sentiment_overall_summary.csv
│ ├── account_sentiment_performance.csv
│ └── side_share_by_sentiment.csv
├── outputs/ # Visual outputs
│ ├── trade_count_by_sentiment.png
│ ├── notional_by_sentiment.png
│ ├── pnl_by_sentiment.png
│ ├── winrate_by_sentiment.png
│ ├── leverage_by_sentiment_box.png
│ ├── side_share_by_sentiment.png
│ ├── accounts_greed_biased.png
│ └── accounts_fear_biased.png
├── ds_report.pdf # Final written report
└── README.md # Project documentation
```

---

## 🚀 How to Run
1. Open the notebooks in **Google Colab**:
   - `notebook_1.ipynb` → data setup, cleaning, merge  

2. Ensure the folder structure is preserved (`csv_files/`, `outputs/`).

3. All outputs (tables & plots) are saved automatically.

---


## 🔗 Open in Colab
- Notebook - (https://colab.research.google.com/drive/1pP_428wu15S2e1JDmQCah8IzBim1vSbr?usp=sharing) 


---

## 🛠️ Reproducibility
At the top of **`notebook_1.ipynb`**, add this cell to ensure the folder structure is always created:

```python
# --- Reproducibility setup ---
import os

CANDIDATE_NAME = "aaysha_sheikh"
ROOT = f"/content/ds_{CANDIDATE_NAME}"
CSV  = f"{ROOT}/csv_files"
OUT  = f"{ROOT}/outputs"

os.makedirs(CSV, exist_ok=True)
os.makedirs(OUT, exist_ok=True)

print("Project root set to:", ROOT)
```

## 📊 Key Metrics
- **Profitability**: total/avg PnL, win rate  
- **Volume**: total notional traded  
- **Risk**: leverage distributions (if present)  
- **Side bias**: share of longs vs shorts  
- **Account performance**: trader-level breakdown by sentiment  

---

## ⚠️ Limitations

- The provided trader dataset and Fear & Greed dataset do not overlap in time.
- As a result, trades appear with classification = Unknown.
- The framework (cleaning, merging, sentiment simplification, summaries, plots, statistical tests) is fully implemented and will produce meaningful insights when applied to overlapping real-time data.
 
---

## ✍️ Author
**Aaysha Sheikh**  
Candidate – Junior Data Scientist (Primetrade.ai Assignment)
