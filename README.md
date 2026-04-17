# Decision Tree vs. Random Forest: Loan Default Prediction

## Project Overview
This project analyzes publicly available loan data from LendingClub.com to build predictive models that classify whether a borrower is likely to pay back their loan in full. The core objective is to compare the performance of a **Decision Tree Classifier** against a **Random Forest Classifier** in a real-world financial context.

## Dataset
The dataset consists of **9,578 entries** with **14 columns**. Key features include:
* **FICO Score**: The credit score of the borrower.
* **Interest Rate**: The interest rate of the loan.
* **Purpose**: The reason for the loan (e.g., debt consolidation, credit card, small business).
* **Not Fully Paid**: The target variable (0 = Paid in full, 1 = Defaulted).

## Analysis & Visualizations
The project includes Exploratory Data Analysis (EDA) to understand the relationship between credit policies and loan outcomes:
* **FICO Distributions**: Comparison of FICO scores across different credit policies.
* **Interest Rates**: Correlation between FICO scores and interest rates charged.
* **Loan Purpose**: Analysis of loan counts by purpose, segmented by repayment status.

## Model Performance
I implemented and evaluated two models using `scikit-learn`. Due to class imbalance (8,045 paid vs. 1,533 defaulted), `class_weight='balanced'` was utilized.

### Comparison Results:
| Metric | Decision Tree | Random Forest |
| :--- | :--- | :--- |
| **Accuracy** | 74% | 85% |
| **Defaults Caught (Recall for Class 1)** | 69 | 1 |

## Summary of Findings
While the **Random Forest** achieved a higher overall accuracy of 85%, it failed to identify risky loans, catching only 1 default. The **Decision Tree**, despite a lower overall accuracy, correctly flagged 69 potential defaults. 

**Conclusion:** In the context of loan lending, the Decision Tree proved more useful as it better identifies high-risk borrowers, even if it is less accurate overall.

## How to Run
1. Ensure you have `pandas`, `numpy`, `scikit-learn`, `matplotlib`, and `seaborn` installed.
2. Clone this repository.
3. Run the Jupyter Notebook `Decision Tree vs Random Forest.ipynb`.
