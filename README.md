## README.md

### Project Title
**Bayesian Optimisation for Credit Scoring Using XGBoost**



###  Project Overview
This project applies Bayesian Optimisation to tune the hyperparameters of an XGBoost model designed to predict credit default risk. The goal is to improve classification performance while maintaining fairness and generalisability across different subgroups.


###  Dataset Used
- **Name**: German Credit Dataset
- **Source**: UCI Machine Learning Repository  
- **Description**: Contains 1,000 examples of loan applicants with 20 features including credit history, purpose of loan, employment status, and more.
- **Target**: Binary classification — whether the applicant is a good or bad credit risk.



###  Model and Optimisation
- **Model**: XGBoost Classifier
- **Optimisation Method**: Bayesian Optimisation (via `skopt`)
- **Hyperparameters Tuned**:
  - `max_depth`
  - `learning_rate`
  - `n_estimators`
  - `subsample`
  - `colsample_bytree`
  - `gamma`
- **Objective Function**: AUC-ROC (Area Under ROC Curve)



###  Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- AUC-ROC


### Folder Structure
```

├── credit_risk_model_UCI.ipynb           # Jupyter notebook with model training and tuning
├── models/                               # Saved model artefacts (optional)
├── README.md                             # Project overview (this file)
├── data_sheet.md                         # Dataset documentation
└── model_card.md                         # Model documentation
├── data/                                 # German credit dataset
```



###  Key Learnings
- Bayesian optimisation outperforms grid/random search in both efficiency and final model performance.
- Proper hyperparameter tuning is crucial when working with imbalanced data.
- Evaluation on subgroup performance (e.g., employment type, age) helps uncover model bias.



###  How to Run
1. Clone the repository
2. Load the German Credit dataset
3. Run `credit_model.ipynb` in `notebooks/`
4. Output includes best parameters, evaluation report, and ROC curve



###  Future Improvements
- Add fairness-aware constraints to the optimisation loop
- Test on LendingClub data for scalability
- Deploy model via REST API for real-time credit scoring
