# 📈 ZBroker Trading Challenge

This repository contains my work for the **ZBroker Trading Challenge** — building, testing, and optimizing trading algorithms on FTSE100 data.  
The aim is to design a reproducible backtesting framework, implement the baseline ZBroker algorithm, and then explore advanced strategies to maximize portfolio performance.

---

## 🚀 Setup Instructions

Clone the repository:
```bash
git clone https://github.com/ledwards9378/zbroker.git
cd zbroker
```

Create and activate a virtual environment:
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Install dependencies:
```powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

---

## 📂 Project Structure

```
zbroker/
  data/
    raw/          # raw downloaded CSVs
    processed/    # cleaned parquet files
  src/
    config.py     # tickers, paths, parameters
    data.py       # data ingestion and saving
    indicators.py # rolling stats, z-scores
    backtest.py   # trading loop
    utils.py      # helper functions
  notebooks/      # exploratory analysis
  tests/          # unit tests
  requirements.txt
  README.md
```

---

## ▶️ Usage

Download initial data:
```powershell
python -m src.data
```

This will:
- Fetch FTSE100 prices via yfinance
- Save raw CSVs into `data/raw/`
- Save a combined dataset into `data/processed/prices.parquet`

Quick sanity check plot:
```powershell
python notebooks/quick_check.py
```

---

## 🎯 Goals

- ✅ Build a reproducible backtesting framework  
- ✅ Implement the baseline ZBroker algorithm  
- 🔄 Scale to the full FTSE100 universe  
- 🔄 Optimize parameters and test advanced strategies  
- 🔄 Deliver a polished GUI + final presentation  

---

## 🛠️ Tech Stack

- **Python 3.11+**  
- **pandas / numpy** — data handling & math  
- **matplotlib / seaborn** — visualization  
- **scipy** — statistics  
- **yfinance** — financial data  
- **pyarrow** — efficient storage (Parquet)  
- **jupyter** — exploration  

---

## 📌 Notes

- Always activate the virtual environment before running scripts:
  ```powershell
  .venv\Scripts\Activate.ps1
  ```
- Large raw data files are ignored by Git (see `.gitignore`).  
- Processed outputs are reproducible from the pipeline.  
```
