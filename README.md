🚦 Road Accident Risk Prediction using Machine Learning
📌 Project Overview

Road accidents are influenced by multiple factors such as road geometry, environmental conditions, traffic rules, and temporal context.
This project aims to predict accident risk using machine learning models based only on pre-accident observable features, making the solution realistic and deployable for real-world use cases such as road safety analysis and preventive planning.

🎯 Objective

Predict a continuous accident risk score

Identify key factors contributing to higher accident risk

Build an interpretable and scalable ML pipeline

📊 Dataset Description

The dataset contains structured information related to road and environmental conditions:

Key Features

Road characteristics: curvature, num_lanes, road_type

Traffic rules: speed_limit

Environmental factors: weather, lighting

Temporal context: time_of_day, holiday, school_season

Safety indicators: road_signs_present, public_road

Target Variable

accident_risk (continuous value)

⚠️ Historical accident count–based features were intentionally excluded from final modeling to avoid target leakage.

🔍 Exploratory Data Analysis (EDA)

EDA was performed to:

Understand feature distributions

Analyze the relationship between road conditions and accident risk

Identify patterns such as increased risk under sharp curvature, poor lighting, and certain speed limits

Detect potential data leakage and unrealistic correlations

Visualizations included:

Distribution plots

Boxplots and violin plots

Feature vs target analysis

🧠 Feature Engineering

Key feature engineering steps included:

Encoding categorical variables using one-hot encoding

Ordinal encoding for ordered features like road curvature

Binary encoding for boolean indicators

Removing features that could leak target information

Ensuring consistency across training and prediction datasets

🤖 Modeling Approach
1️⃣ Baseline Model – Random Forest Regressor

Used as the initial model due to its robustness and ability to capture non-linear relationships

Provided strong baseline performance

Helped identify feature importance and potential data issues

2️⃣ Improved Model – XGBoost Regressor

Implemented to improve predictive performance

Better handled feature interactions and complex patterns

Achieved lower error and improved generalization compared to Random Forest

📏 Model Evaluation

Models were evaluated using:

Mean Absolute Error (MAE)

R² Score

Actual vs Predicted scatter plots to verify realistic model behavior

Special attention was given to avoid misleadingly perfect results caused by data leakage.

📈 Key Insights

Road curvature is a strong contributor to accident risk

Poor lighting conditions significantly increase risk

Speed limits interact with road geometry rather than acting independently

Proper feature selection is critical for realistic predictions

🛠️ Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

XGBoost

🚀 Future Improvements

Convert regression output into risk categories (Low / Medium / High)

Add explainability using SHAP values

Deploy as a web app using Streamlit or FastAPI

Incorporate real-time weather or traffic data

📌 Conclusion

This project demonstrates an end-to-end machine learning workflow, from data analysis and feature engineering to model selection and evaluation.
A key highlight of the project is the identification and removal of target leakage, resulting in a realistic, interpretable, and deployable accident risk prediction system.
