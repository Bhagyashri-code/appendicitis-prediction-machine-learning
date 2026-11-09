# appendicitis-prediction-machine-learning
Appendicitis Diagnosis Prediction Using Machine Learning
Project Overview
This academic machine learning project compares Random Forest and L1-regularized Logistic Regression (Lasso) for predicting appendicitis diagnosis from clinical indicators. The project explores predictive performance, model overfitting, hyperparameter tuning, and interpretability.
Project type: Academic analysis and model comparison. The results below are reported in the project presentation and have not been independently reproduced here. This project is not a clinically validated diagnostic tool.

Problem Statement
Evaluate whether clinical indicators can help distinguish appendicitis from non-appendicitis cases, and compare a nonlinear ensemble model with a more interpretable regularized linear model.
Objectives
- Train and evaluate a baseline Random Forest classifier.
- Investigate overfitting and optimize Random Forest hyperparameters.
- Reduce less informative features and consider potential data leakage.
- Compare Random Forest against L1-regularized Logistic Regression.
- Examine influential features and the trade-off between predictive performance and interpretability.
Methods and Workflow
1. Baseline Random Forest
- Target: Diagnosis.
- Predictors: available indicative variables, including age and BMI.
- Train/test split: 70% / 30% (train_test_split(test_size=0.3)).
- Initial settings: n_estimators=100, max_depth=None.
- Observation: training performance reached 1.00, raising concerns about overfitting.
- 2. Random Forest Hyperparameter Tuning
- A train/test AUC gap persisted in this stage, motivating further simplification.
3. Feature-Reduced Random Forest
A subsequent experiment reduced less informative features and explored shallower trees
Alvarado_score and Length_of_stay were excluded to address concerns about derived variables and information unavailable at prediction time. The presentation describes five-fold cross-validation in this stage.
4. L1-Regularized Logistic Regression
- Scaled the data and used seven selected features.
- Applied L1 regularization to shrink some feature coefficients to zero.
- Compared performance and interpretability against Random Forest.
- Interpretation: The reported Random Forest model achieved higher test ROC-AUC. L1 Logistic Regression offers a more directly interpretable coefficient-based model. These metrics come from the presentation; exact reproducibility requires the dataset, code, split settings, and selected hyperparameters.
