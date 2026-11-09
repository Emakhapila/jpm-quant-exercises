# JPM Quantitative Research Exercises

This repository contains a collection of quantitative research and risk modeling exercises, including:

- Natural gas price modeling and storage contract valuation  
- Credit risk modeling (PD + Expected Loss)  
- FICO score bucketing using quantization techniques  

---

## 📁 Project Structure

```
jpm-quant-exercises/
├── nat_gas_storage/
│   ├── data/        # Natural gas price CSV
│   ├── src/         # Price curve + storage pricing code
│   └── notebooks/   # Exploratory notebooks
└── credit_risk/
    ├── data/        # Loan dataset
    ├── src/         # PD model + FICO bucketing code
    └── notebooks/   # Exploratory notebooks
```

---

##  Natural Gas Modeling (Tasks 1 & 2)

### Task 1 — Price Curve Construction  
- Trend + seasonality model  
- Spline interpolation for daily estimates  
- `estimate_price(date)` returns a price for any date  

### Task 2 — Storage Contract Pricing  
- Injection/withdrawal schedules  
- Storage costs, injection/withdrawal fees  
- `price_storage_contract(...)` returns contract value  

---

##  Credit Risk Modeling (Tasks 3 & 4)

### Task 3 — Probability of Default (PD)  
- Logistic regression model  
- Expected Loss = PD × LGD × EAD  
- `expected_loss(...)` computes EL for any borrower  

### Task 4 — FICO Bucketing  
- MSE-based quantization  
- Log-likelihood-based quantization (PD-aware)  
- Produces rating buckets for ML models  

---

##  Requirements

```
pandas
numpy
scikit-learn
scipy
matplotlib
```


Install using:

```bash
pip install -r requirements.txt
```


---

##  Usage

Example:

```python
from nat_gas_storage.src.price_model import estimate_price
from credit_risk.src.pd_model import train_pd_model
from credit_risk.src.fico_bucketing import fico_buckets_loglik
```
