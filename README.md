  # 📊 E-commerce Sales Forecasting with SARIMA

  > Time series analysis and sales forecasting using statistical modeling

  [![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
  [![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

  ## 📝 Project Overview

  This project demonstrates **time series forecasting** applied to e-commerce sales data. Using the **SARIMA** (Seasonal
  AutoRegressive Integrated Moving Average) model, I predict future sales trends based on historical patterns.

  **Dataset**: [Kaggle SuperStore Sales Dataset](https://www.kaggle.com/)
  **Why this project**: After 4 years in e-commerce using Google Analytics daily, I wanted to apply statistical forecasting to
  understand sales patterns and predict future trends.

  ---

  ## 🎯 Objectives

  1. **Exploratory Data Analysis**: Identify top-performing products, regions, and customer segments
  2. **Correlation Analysis**: Test relationships between sales and various business dimensions
  3. **Time Series Decomposition**: Separate trend, seasonality, and residuals
  4. **Forecasting**: Build a SARIMA model to predict sales for the next 7 days

  ---

  ## 🔍 Key Findings

  ### Business Insights

  - **Technology products** generate the highest revenue (33% of total sales)
  - **California and New York** are the top-performing states
  - **Standard shipping** accounts for 60% of revenue
  - **Consumer segment** represents 50%+ of total sales

  ### Statistical Analysis

  - **Stationarity Test**: ADF test confirms the series is stationary (p-value < 0.05)
  - **Seasonality**: Clear seasonal patterns detected with 12-month cycle
  - **Model Selection**: SARIMA(1,1,1)(1,1,1,12) chosen via grid search (lowest AIC: 20738.35)
  - **Model Performance**: RMSE = 267.66 (±12% error rate)

  ### Correlation Analysis

  Tested correlations between Sales and:
  - Customer Segments → No strong correlation
  - Product Categories → No strong correlation
  - Shipping Modes → No strong correlation

  **Conclusion**: Other factors (pricing, seasonality, promotions) likely have more impact on sales.

  ---

  ## 🛠️ Tech Stack

  - **Python 3.8+**
  - **Pandas** - Data manipulation
  - **NumPy** - Numerical computations
  - **Matplotlib & Seaborn** - Data visualization
  - **Statsmodels** - Time series analysis & SARIMA
  - **Scikit-learn** - Model evaluation (RMSE)

  ---

  ## 📊 Methodology

  ### 1. Data Preparation
  - Converted dates to datetime format
  - Handled missing values (Postal Code)
  - Sorted data by Order Date
  - Resampled to daily averages with linear interpolation

  ### 2. Exploratory Analysis
  - Sales by Category, Product, State, Customer
  - Revenue by Shipping Mode
  - Top 10 products and clients

  ### 3. Time Series Analysis
  ```python
  # Stationarity test
  ADF Statistic: -20.81 (p-value: 0.0)
  → Series is stationary

  # Decomposition
  - Trend: Stable growth over time
  - Seasonality: 12-month pattern detected
  - Residuals: Random noise

  4. SARIMA Model

  # Grid search tested 64 parameter combinations
  Best model: SARIMA(1,1,1)(1,1,1,12)
  AIC: 20738.35
  RMSE: 267.66

  5. Forecasting

  7-day forecast with confidence intervals:
  2019-01-01: $241
  2019-01-02: $244
  2019-01-03: $229
  2019-01-04: $196
  2019-01-05: $254 (peak)
  2019-01-06: $223
  2019-01-07: $229

  ---
  💡 Business Recommendations

  Based on this analysis, here's what I would recommend:

  1. Inventory Planning
  → Stock high-demand tech products ahead of predicted sales peaks
  2. Marketing Campaigns
  → Concentrate ad spend during high-traffic periods (Sundays show +40% sales)
  3. Regional Focus
  → Prioritize California and New York for promotions (highest revenue states)
  4. Customer Retention
  → Focus on Consumer segment (50%+ of revenue) with loyalty programs
  5. Shipping Strategy
  → Standard shipping is preferred (60% of orders) → optimize this channel

  ---
  📁 Project Structure

  analyse-ventes-ecommerce-sarima/
  │
  ├── README.md                          # This file
  ├── sales_forecasting_sarima.ipynb     # Main Jupyter notebook
  └── data/
      └── train.csv                      # Dataset 

  ---
  🚀 How to Run

  1. Clone the repository
  git clone https://github.com/Heltondsm/analyse-ventes-ecommerce-sarima.git
  cd analyse-ventes-ecommerce-sarima

  2. Install dependencies
  pip install pandas numpy matplotlib seaborn statsmodels scikit-learn jupyter

  4. Run the notebook
  jupyter notebook sales_forecasting_sarima.ipynb

  ---
  📈 Sample Visualizations

  Sales by Category
  Technology products dominate revenue with $836K (33% of total sales)

  Time Series Decomposition
  Clear trend and 12-month seasonal patterns detected

  SARIMA Diagnostics
  Residuals show normal distribution, confirming model validity

  7-Day Forecast
  Predictions with 95% confidence intervals

  ---
  🎓 Skills Demonstrated

  - ✅ Exploratory Data Analysis (EDA)
  - ✅ Data Cleaning & Preprocessing
  - ✅ Statistical Testing (ADF test)
  - ✅ Time Series Decomposition
  - ✅ SARIMA Modeling
  - ✅ Hyperparameter Tuning (Grid Search)
  - ✅ Model Validation (RMSE, diagnostics)
  - ✅ Data Visualization
  - ✅ Business Insights Translation

  ---
  📫 Contact

  Helton Dos Santos Moreira
  Data Analyst | 4 years e-commerce experience + analytics

  https://www.linkedin.com/in/helton-dsm-data
  heltonmail8@gmail.com

  ---
  📄 License

  This project is for educational and portfolio purposes.

  ---
  ⭐ If you found this analysis useful, please consider starring the repo!
