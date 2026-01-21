# Medical Insurance Cost Prediction & Risk Control
A machine learning framework to predict insurance claim behaviour and amounts, helping insurers mitigate risks and improve profitability.

## Project Overview
- **Business Problem**: A medical insurance company suffered a $79.56M loss from 10k transactions; need to identify high-risk claims and optimize operations.
- **Goal**: Predict whether customers will file claims (classification) and the claim amount (regression) to support risk control.
- **Dataset**: Kaggle medical insurance dataset (100k+ records, 54 variables) covering demographics, lifestyle, health conditions, and insurance details.

## Methodology
### Data Processing
- Handled missing values (semantic filling for `alcohol_freq`), deleted redundant/leakage features (e.g., `monthly_premium`, `person_id`).
- Encoded categorical variables via dummy transformation; split data into training (80%)/test (20%) sets; standardized features for model compatibility.
- Constructed binary target variable `claimed` (1 = claim occurred, 0 = no claim) based on `total_claims_paid`.

### Models
| Model Type       | Models Used                  | Purpose                                  |
|------------------|------------------------------|------------------------------------------|
| Classification   | Logistic Regression, XGBoost Classifier | Predict if a customer will file a claim  |
| Regression       | Linear Regression, Random Forest, XGBoost Regressor | Predict claim amount for claimants       |
| Two-stage Model  | XGBoost (Classification + Regression) | End-to-end claim prediction & amount estimation |


![mechanism_of_project](https://github.com/YanhuaB/Medical_Insurance_Risk_Control_Project/blob/main/mechanism.jpg)
## Key Results
- **Best Model**: XGBoost (balanced accuracy, stability, and generalization; Train R²=0.31, Test R²=0.26).
- **Key Predictors**: Chronic condition count, past 3-year hospitalization days, last-year visits, risk score.
- **Commercial Value**: Generated $16.24M total value by reducing losses; transformed a $15.58M loss into a $657.76k profit for 20k transactions.
- **Operational Optimization**: Enabled data-driven resource allocation (dedicated teams for high-risk cases, automation for low-risk).

## Future Directions
- Incorporate long-term customer claim history to improve prediction accuracy.
- Enhance feature engineering to address the randomness of unforeseeable events (e.g., accidents, acute illnesses).

## Team & Credit
- **Team**: FMG
- **Members**: Bai Yanhua, Hong Kenan, Huang Yunxiu, Cao Yifang, Guo Jiayi, Luo Ya
## Institution: City University of Hong Kong
- **Course**: IS6400

## Links
If you would like to learn more details about our project, you can check the link below.  
| [Dataset](https://github.com/YanhuaB/Medical_Insurance_Risk_Control_Project/blob/main/Code/medical_insurance.csv) | [Full Project Code](https://github.com/YanhuaB/Medical_Insurance_Risk_Control_Project/blob/main/Code/medical_insurance_cost_prediction&risk_control.ipynb) | [Report](https://github.com/YanhuaB/Medical_Insurance_Risk_Control_Project/blob/main/Formal%20Report/report.docx) |

