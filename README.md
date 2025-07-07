# xgb_calories
This project uses a Gradient Boosting Regressor to predict the number of calories burned during physical activity based on features like age, gender, weight, duration, and heart rate. The model is trained and evaluated using scikit-learn, providing insights into exercise energy expenditure.

# 🔍 Feature Engineering & Model Insights
#
# This notebook demonstrates a structured approach to improving calorie expenditure prediction using
# Gradient Boosting (XGBoost). The workflow includes:
#
# - Generation of domain-informed features such as BMI.
# - Systematic creation of pairwise interaction terms to capture nonlinear relationships between variables.
# - Careful consideration of model complexity and overfitting risk through selective feature crosses.
# - Evaluation of feature importance via incremental model versions (v1–v5), tracking RMSE performance:
#
#     - v1: Baseline model with raw features – Final CV RMSE: 0.101
#     - v3: Added multiplication and division terms (later removed division due to no improvement) 
#     - v4: Added BMI – improved explainability with consistent performance
#     - v5: Combined BMI and cross features – (Final RMSE shown below, ~0.0600)
#
# - Model tuning using early stopping, regularization (`gamma`, `max_delta_step`), and 8-fold cross-validation.
# - Efficient training time (~59 seconds/fold on GPU) and stable model convergence by iteration ~400.
#
# ✅ Final Result:
# The final model achieved a cross-validated RMSE of ~0.0600, indicating strong predictive accuracy.
# The feature engineering process contributed significantly by enhancing the model's ability to learn
# meaningful interactions without overfitting.
#
# This workflow balances performance, interpretability, and computational efficiency, demonstrating
# effective use of structured data and model diagnostics.
