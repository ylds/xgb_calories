# 🔍 Feature Engineering & Model Insights

This project demonstrates a structured approach to improving calorie expenditure prediction using Gradient Boosting (XGBoost). The workflow includes:

* 🏋️‍♂️ **Domain-informed features** such as BMI calculation

* 🔗 **Pairwise interaction terms** to capture nonlinear relationships

* ⚖️ **Model complexity control** to avoid overfitting via selective feature crosses

* 📊 **Incremental model evaluation** across versions (v1–v5), tracking RMSE:

  * 🚀 **v1:** Baseline model with raw features – Final CV RMSE: 0.101
  * 🔄 **v3:** Added multiplication and division terms (division removed later)
  * 📈 **v4:** Added BMI – improved explainability & consistent performance
  * 🎯 **v5:** Combined BMI and cross features – Final RMSE \~0.0600

* ⏱️ **Model tuning** with early stopping, regularization (`gamma`, `max_delta_step`), and 8-fold cross-validation

* ⚡ **Efficient training time** (\~59 seconds/fold on GPU) and stable convergence around iteration 400

---

## 🏆 Final Result

The final model achieved a cross-validated RMSE of approximately **0.0600**, indicating strong predictive accuracy. Feature engineering significantly enhanced the model’s ability to learn meaningful interactions without overfitting.

## EDA

Distribution of the calories
<img width="730" height="566" alt="image" src="https://github.com/user-attachments/assets/6041a760-abb7-4d4e-9eb1-da74fd479e9e" />



