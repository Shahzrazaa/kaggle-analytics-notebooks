# Kaggle Analytics Notebooks: E-commerce, Ads & Churn

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

GitHub mirror of my four public Kaggle notebooks. Each one answers a business question an e-commerce, marketing or CRM team actually asks, and ends with recommended actions. The notebooks are stored **with their outputs**, so the charts render right here on GitHub.

| # | Notebook | Business question | Key result | Kaggle |
|---|---|---|---|---|
| 1 | [E-commerce RFM Segmentation & Cohort Retention](notebooks/e-commerce-rfm-segmentation-cohort-retention.ipynb) | Which customers drive revenue, who is about to churn, and where should a retention budget go? | Top 20% of customers = 77% of revenue; only ~19% of new customers buy again the next month | [Open](https://www.kaggle.com/code/shahzadrazaa/e-commerce-rfm-segmentation-cohort-retention) |
| 2 | [PPC Wasted-Spend Audit: CPA, ROAS & Reallocation](notebooks/ppc-wasted-spend-audit-cpa-roas-reallocation.ipynb) | How much ad budget goes to ads that never convert, and what would simple rules recover? | 25% of spend went to ads with zero approved sales; 3 rules project +48% sales at the same budget (to be tested) | [Open](https://www.kaggle.com/code/shahzadrazaa/ppc-wasted-spend-audit-cpa-roas-reallocation) |
| 3 | [Retail Sales KPI Dashboard + 12-Month Forecast](notebooks/retail-sales-kpi-dashboard-12-month-forecast.ipynb) | What is driving growth, how seasonal is it, and what should we plan for next year? | Growth is volume-driven (+28% orders, -6% AOV); Holt-Winters backtest MAPE 20.8% | [Open](https://www.kaggle.com/code/shahzadrazaa/retail-sales-kpi-dashboard-12-month-forecast) |
| 4 | [Bank Churn: XGBoost, SHAP & Profit Targeting](notebooks/bank-churn-xgboost-shap-profit-targeting.ipynb) | Which customers should get a retention offer so the bank makes the most money? | Test ROC-AUC 0.871 (vs 0.776 logistic); expected-value targeting beats "contact everyone" by $46k under stated assumptions | [Open](https://www.kaggle.com/code/shahzadrazaa/bank-churn-xgboost-shap-profit-targeting) |

## Data

All four use public Kaggle datasets (not included in this repo):

| Notebook | Dataset |
|---|---|
| 1 | [Online Retail II (UCI)](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) |
| 2 | [Sales Conversion Optimization](https://www.kaggle.com/datasets/loveall/clicks-conversion-tracking) |
| 3 | [Sales Forecasting (Superstore)](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting) |
| 4 | [Churn Modelling](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling) |

## Run locally

```bash
pip install -r requirements.txt
# download the dataset CSVs into ./data (any subfolder works)
jupyter notebook notebooks/
```

Each notebook looks for its CSV under `/kaggle/input`, `../input` or `./data`, so it runs unchanged on Kaggle or locally. The easiest path is to open the Kaggle link and click **Copy & Edit**.

## Notes

- Where a dataset lacks a business input (revenue per conversion in #2, customer value and offer cost in #4), the notebook states the assumption in a clearly labelled variable you can change.
- Results come from the notebook outputs as published; re-running with newer library versions can shift numbers slightly.

## Related

- [amazon-ppc-search-term-audit](https://github.com/Shahzrazaa/amazon-ppc-search-term-audit): the PPC audit from notebook #2 turned into a reusable CLI for Amazon search-term reports
- [customer-churn-retention-strategy](https://github.com/Shahzrazaa/customer-churn-retention-strategy): the original 2019 churn project that notebook #4 rebuilds

---

**Author:** [Shahzad Raza](https://github.com/Shahzrazaa) · [Kaggle](https://www.kaggle.com/shahzadrazaa) · MIT License (code); datasets keep their own licenses
