# Machine Learning Enhanced Statistical Arbitrage

This repository contains a complete, research-grade **statistical arbitrage trading system** that integrates classical econometrics with modern machine learning.

Built as a unified Jupyter notebook, the project covers:
- K-means clustering for universe structuring
- Cointegration-based pair selection
- PCA factor modeling
- Mean reversion diagnostics (ADF, Hurst, half-life)
- Feature-engineered ML timing signals using LightGBM
- Walk-forward time-series validation
- Realistic backtesting with transaction costs and slippage

Designed for **academic research**.

---

## 📌 Key Features

### **1. Statistical Foundations**
- K-means for clustering correlated stocks
- Hedge ratio estimation via multivariate regression
- PCA to extract market/sector factors
- Spread modeling using AR(1) half-life estimation
- MVN & autocorrelation diagnostics

### **2. Cointegration & Mean Reversion**
- Engle–Granger two-step test (5% significance)
- Johansen test for multi-asset cointegration
- Half-life computation via AR(1)
- Hurst exponent validation (< 0.5)

### **3. Machine Learning Enhancements**
- LightGBM classifier for entry/exit timing
- ~50 engineered features (lagged, technical, volatility, regime)
- Zero data leakage (all features shift-adjusted)
- Walk-forward cross-validation for time-series integrity
- Mean AUC ≈ **0.92** across tested pairs

### **4. Backtesting Framework**
- 10 bps transaction cost + 5 bps slippage
- 10% capital allocation per trade
- Probability-filtered ML trading signals
- Baseline statistical arbitrage comparison
- Sharpe, drawdown, returns, distributions, equity curves

---

## 📊 Results Summary

- **Average AUC:** 0.92
- **ML vs Baseline Sharpe Improvement:** +2.6%
- ML signals produced **higher quality trades** and fewer false signals
- Combined statistical + ML approach beat classical stat-arb on:
  - Win rate
  - Risk-adjusted returns
  - Stability across folds

---

## 📁 Repository Structure
```
/
├── StatArb_MLproject.ipynb                      # Complete unified workflow
├── data/                               # Price data + intermediate CSVs
├── plots/
├── README.md
├── .gitignore
└── LICENSE
```

---

## 🔧 Technologies Used

- Python
- NumPy, Pandas, SciPy
- scikit-learn
- LightGBM
- Statsmodels
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 📄 License

MIT License — free for academic and personal use.

---

## 🙌 Acknowledgments

This project integrates core methods from econometrics, machine learning, and quantitative finance, inspired by academic literature and professional trading frameworks.
