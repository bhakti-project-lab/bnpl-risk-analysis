# Risk-Based Revenue Optimization in BNPL

**Problem**
A Buy-Now-Pay-Later (BNPL) lending portfolio showed strong user growth, but revenue was not scaling proportionally. The objective was to identify revenue leakage and understand whether high-risk customer approvals were impacting profitability.

**Approach**
_Data Preparation_
Cleaned and processed loan-level data of 31K+ records
Created key metrics such as:
1. Interest earned
2. Actual profit per loan

_SQL-Based Analysis_
1. Segmented customers by:
-Age groups
-Income levels
-Loan-to-Income ratio (LPI)
-Past default history
2. Identified high-risk segments contributing to negative profit

_Risk Modeling using Python_
1. Built a Logistic Regression model to predict probability of default
2. Features used:
-Income
-Loan amount
-Loan-to-income ratio
-Age
-Past default history
3. Model performance: AUC = 0.86

_Risk Simulation_
1. Ranked all loans based on predicted risk
2. Simulated a risk-based approval strategy by removing top 20% high-risk loans
3. Compared portfolio performance before and after filtering

**Key Results**
Default Rate reduced from 21.6% → 9.46%
Total Loss reduced by ~97% (₹5.04 Cr → ₹0.14 Cr)
Profit per loan improved from -₹1599 → -₹57
Loan volume reduced by ~20% (highlighting growth vs risk trade-off)

**Key Insights**
High loan-to-income ratio (>30%) is the strongest driver of defaults
Past defaulters show significantly higher repeat default rates
Revenue leakage is caused by overexposure to high-risk borrowers, not low income alone
Risk-based approval strategies can significantly improve portfolio stability

**Tools & Technologies**
Python: Pandas, NumPy, Scikit-learn
SQL: Data segmentation & aggregation
Jupyter Notebook: Analysis & modeling
