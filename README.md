# Sales Analysis and Forecasting for E-Commerce Platforms

## Project Overview
This project aims to enhance e-commerce platform performance by leveraging sales data to identify trends, predict future sales, and support merchants in crafting effective strategies. Using historical data from May 2016 to April 2019, this analysis combines machine learning, time series modeling, and statistical methods to deliver actionable insights.

---

## Dataset
The dataset comprises sales data across various clothing categories. Features include:
- **S (Sales)**: Sales volume (unit: billion Yuan)
- **X4**: Page views (unit: billion)
- **X8**: Additional purchases (unit: 10 million)
- **X9**: Customer group index (unit: 100 thousand)
- **X10**: Transaction index (unit: million)

---

## Key Analyses

### 1. **Data Cleaning**
   - Removed duplicates and handled missing values using imputation.

### 2. **Outlier Detection**
   - Identified outliers through boxplots and Z-scores.
   ![Pants Outliers](images/pants_outliers.png)
   ![Dress Outliers](images/dress_outliers.png)
   ![Sweater Outliers](images/sweaters_outliers.png)

### 3. **Feature Scaling**
   - Standardized features using Z-score normalization for consistent scaling.

### 4. **Correlation Analysis**
   - Explored inter-feature relationships via heatmaps and scatter plots.
   ![Pants Correlation Matrix](images/pants_sales_x_other_variables.png)
   ![Dress Correlation Matrix](images/dress_sales_x_other_variables.png)
   ![Sweater Correlation Matrix](images/sweater_sales_x_other_variables.png)

### 5. **Principal Component Analysis (PCA)**
   - Dimensionality reduction to simplify the dataset while retaining over 95% of the variance.
   ![Pants Feature Selection](images/pants_feature_selection.png)
   ![Dress Feature Selection](images/dress_feature_selection.png)
   ![Sweater Feature Selection](images/sweater_feature_selection.png)

---

## Prediction Models

### **Synthetic Time Series**
   - Created a synthetic time series with added trend and seasonality to simulate sales data.  
   - Used this synthetic series as the foundation to build and enhance the main time series for further analysis.  
   ![Synthetic Time Series](images/synthetic_time_serie.png)

### **Time Series Modeling**
#### **Time Series Decomposition**
   - Decomposed the main time series into trend, seasonal, and residual components for analysis.  
   ![Time Series Decomposition](images/time_serie_decomposition.png)

#### **Holt-Winters Exponential Smoothing**
   - Built a forecasting model using Holt-Winters Exponential Smoothing.  
   - Captured seasonal trends and forecasted future sales with high accuracy.  
   ![Pants Sales Over Time](images/pants_time_serie.png)  
   ![Holt-Winters Forecast vs Actual](images/pants_training_x_testing_x_forcast.png)  
   ![Forecast Residuals](images/forcast_residuals.png)

#### **ARIMA**
   - Built and fine-tuned ARIMA models for advanced time series forecasting.
   - Leveraged residual analysis to validate model predictions.
   - ![ARIMA Model Forecast](images/arima_forecast.png)

---

### **Linear Regression**
   - Implemented **Linear Regression** to predict sales using key features.
   - Evaluated model performance using R² scores and compared predicted sales with actual sales.
   - Provided functionality to predict sales for a specific date and category based on input features.
   ![Pants Sales Real vs Predicted](images/pants_real_x_predicted.png)
   ![Dress Sales Real vs Predicted](images/dress_sales_real_x_predicted.png)
   ![Sweater Sales Real vs Predicted](images/sweater_sales_real_x_predicted.png)
   ![Pants Accuracy](images/pants_accuracy.png)
   ![Dress Accuracy](images/dress_accuracy.png)
   ![Sweater Accuracy](images/sweater_accuracy.png)

---

## Results
- The **Linear Regression** model delivered high R² values across categories, reflecting accurate feature-based predictions.
- **Holt-Winters** effectively captured seasonal variations in sales data.
- **ARIMA** demonstrated robust forecasting for future sales with validated residuals.
- **Synthetic Time Series** provided an adaptable foundation for time series analysis.
- Visualizations highlighted trends, outliers, and predicted versus actual sales.

---

## Visualizations
The notebook includes:
- Detailed boxplots for outlier detection.
- Heatmaps to examine feature correlations.
- PCA plots for feature selection.
- Decomposition plots showcasing trends and seasonality.
- Forecasting charts comparing predictions to actual sales data.

---

