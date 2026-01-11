# Credit Risk Early Warning System (NIFTY 50)

This repository contains a Jupyter notebook that implements an early warning system for monitoring credit and market risk in equity portfolios, using NIFTY 50 stocks as a case study.

The goal of the project is to demonstrate how multiple simple risk indicators can be combined with a lightweight machine learning model to flag periods of elevated risk in a structured and interpretable way.

---

## 1. Key Features

- Volatility monitoring using rolling statistics  
- Beta drift detection relative to the NIFTY 50 index (^NSEI)  
- Drawdown-based risk thresholds  
- Rolling return Z-score analysis  
- Unsupervised anomaly detection using Isolation Forest  
- Automated email alerts based on a composite risk framework  

---

## 2. Methodology Overview

The system tracks several independent risk signals derived from historical price data. Rather than relying on a single indicator, alerts are generated only when multiple signals confirm elevated risk, or when a machine learning anomaly is detected.

This approach helps reduce false positives and mirrors how early warning systems are typically designed in practice.

---

## 3. Data Source

- Historical price data is downloaded using the `yfinance` library.
- Adjusted closing prices are used to account for corporate actions.
- No market data is stored or committed to this repository.

---

## 4. Alerting & Security

Email alerts are implemented using Gmail SMTP.  
For security reasons, all credentials are loaded via environment variables and are **not included** in the repository.

Refer to the notebook for instructions on setting up email alerts locally.

---
## 5. Key Visualizations

## Repository Structure
- plots\
- src\ main jupyter notebook
- .gitignore
- readme.md
- requirements.txt

