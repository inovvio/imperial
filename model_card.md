## Model Card for XGBoost Credit Risk Classifier

---

### Model Details

**Model Type:** XGBoost Classifier  
**Version:** 1.0  
**Trained On:** German Credit Dataset (UCI)  
**Task:** Binary classification (default risk prediction)

---

### Intended Use

**Primary Users:**
- Risk analysts
- Data scientists
- Financial institutions

**Use Cases:**
- Assessing creditworthiness of applicants
- Supporting loan approval decisions

**Out-of-scope Use:**
- Real-time decisioning without fairness validation
- Predicting loan amounts or interest rates

---

### Performance Summary

**Evaluation Metrics Used:**
- Accuracy: ~77%
- Precision: ~70%
- Recall: ~60%
- AUC-ROC: ~0.83

**Validation Strategy:**
- Stratified 5-fold cross-validation
- Bayesian hyperparameter tuning with Expected Improvement acquisition

---

### Training Data

**Dataset Name:** German Credit Dataset  
**Size:** 1,000 rows x 20 columns  
**Target Classes:** 1 (Good Credit), 0 (Bad Credit)

**Preprocessing Applied:**
- Label encoding
- Feature scaling (StandardScaler)
- Class balancing using `scale_pos_weight`

---

### Ethical Considerations

**Fairness Risks:**
- Possible bias based on employment status or gender
- Data collected historically, not representative of all populations

**Mitigations:**
- Subgroup performance was monitored
- Fairness metrics flagged for future integration

**Recommendations:**
- Retrain with modern, diverse datasets
- Apply fairness-aware learning methods

---

### Limitations
- Small dataset size may reduce generalisation
- Class imbalance impacts recall for minority class
- Model not audited for real-world financial compliance

---

### Caveats and Recommendations
- Use in sandbox/testing only — not yet production-ready
- Interpretability tools (e.g., SHAP) recommended for deployment
- Requires external fairness audit before live deployment

---

### Contact
For more details, contact the project owner or refer to the README file in the project repository.