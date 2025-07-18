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

The final model achieved a cross-validated RMSE (Root Mean Squared Error) of approximately 0.0600, which means its predictions were very close to the actual results. This strong accuracy came from applying feature engineering — the process of creating new, meaningful variables from the data. It allowed the model to capture important interactions between factors, like how a person’s age and job type together influence the likelihood of subscribing, all while avoiding overfitting.

## EDA

Distribution of the calories, right tailed.

<img width="730" height="566" alt="image" src="https://github.com/user-attachments/assets/6041a760-abb7-4d4e-9eb1-da74fd479e9e" />

The correlation matrix reveals strong relationships between weight and height, as well as heart rate and duration. These patterns suggest potential for pairwise interactions, where combining these features could enhance the predictive power of the model.

<img width="842" height="752" alt="image" src="https://github.com/user-attachments/assets/0008acfb-e093-4a00-9f8f-dc89717e6b8e" />

