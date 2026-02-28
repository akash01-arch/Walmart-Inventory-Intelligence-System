🏢 Project Overview
Domain: Retail Supply Chain & Inventory Management.

Objective: Develop an end-to-end ML system to predict demand, classify stockout risks, and optimize inventory levels.

Business Value: Aims to reduce lost revenue caused by stockouts and minimize working capital tied up in overstock.

🏗️ Technical Architecture
The project follows a modular pipeline designed for production readiness:

Raw Data Ingestion: Handles structured retail datasets (CSV format).

Production-Grade Pipeline: Includes a cleaning engine that handles missing values (e.g., promotion_type), fixes data types, and removes duplicates.

Feature Engineering: Creates time-series features (day of week, weekend flags, month) and business metrics like revenue, forecast_bias, and stock_health.

Analytics & Optimization: Integrates an EOQ (Economic Order Quantity) model for inventory optimization and quantifies business impact.

🤖 Machine Learning Models
The system utilizes multiple modeling approaches for different business needs:

Demand Forecasting (Regression): Linear Regression, Ridge, Random Forest, and Gradient Boosting.

Stockout Risk (Classification): Random Forest and Gradient Boosting Classifiers.

Advanced Techniques: Employs TimeSeriesSplit for cross-validation, RandomizedSearchCV for hyperparameter tuning, and SHAP for model explainability.

📊 Key Business Reports & Insights
Executive KPI Dashboard: Visualizes critical metrics like total sales, inventory turnover, and department performance.

30-Day Revenue Forecast: Predicts future earnings based on historical demand patterns.

Inventory Quality Report: Categorizes stock health and identifies excess inventory vs. lost sales revenue.

🛠️ Tech Stack
Languages/Libraries: Python, Pandas, Scikit-learn, Matplotlib, Seaborn.

Storage/Persistence: joblib for model serialization and os for structured reporting.

🚀 Future Roadmap
Deploy real-time predictions via FastAPI.

Enhance models using XGBoost or LightGBM for better accuracy.

Integrate experiment tracking using MLflow.

Author Akash More
