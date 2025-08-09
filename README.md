# Customer Growth Forecasting using SARIMA

This project demonstrates a time series forecasting pipeline to predict future customer reservations for restaurants. Using historical reservation data, a **Seasonal Autoregressive Integrated Moving Average (SARIMA)** model was developed to forecast visitor numbers, providing actionable insights for business planning.

---

### 🎯 **Project Goal & Key Highlights**

The primary goal of this project was to forecast future customer growth (visitor reservations) for restaurants. This project showcases proficiency in the following areas:

* **Comprehensive Data Handling**: Integrated and cleaned raw data from three separate sources to create a unified time series dataset.
* **Time Series Analysis**: Identified and visualized **seasonal patterns** (weekly and monthly) in customer visitation data to inform model selection.
* **Predictive Modeling**: Applied a **SARIMA model** for forecasting, demonstrating an understanding of core time series techniques.
* **Critical Evaluation & Problem Solving**: Thoroughly evaluated model performance using **MAPE** and proposed actionable next steps for improvement, highlighting analytical rigor and strategic thinking.

---

### 🛠️ **Technical Approach**

#### **Data Analysis & Preprocessing**

* **Data Sources**: Consolidated three interconnected datasets, using `reserve_visitors` as the primary target variable.
* **Data Cleaning**: Addressed initial data quality issues, including a date format error, and handled outliers through visualization.
* **Feature Engineering**: Engineered `dayofweek` and `month` features to better capture seasonal trends in the data.

#### **SARIMA Forecasting Model**

* A **SARIMA model** was chosen to leverage the observed seasonality.
* **Parameter Tuning**: The `pmdarima.auto_arima` library was used to automatically identify the optimal model parameters with a seasonal period (**m=7**).
* **Forecasting**: The model was trained on historical data and used to generate a **31-day forecast**.

---

### 📈 **Results & Future Improvements**

The initial **SARIMA model** produced a **MAPE of 459.21%**, indicating its limitations with the current data and features. This result highlights the need for an iterative and robust approach to forecasting challenges.

#### **Next Steps to Improve Accuracy:**

* **Multivariate Modeling (SARIMAX)**: Incorporate external variables like **holidays**, **promotions**, and **weather** to capture their impact on reservations.
* **Enhanced Data Handling**: Implement more sophisticated outlier handling and advanced feature engineering, such as **lagged values** and **rolling statistics**.
* **Model Exploration**: Investigate alternative forecasting models like **Prophet**, **Gradient Boosting** (e.g., **XGBoost**), or **Neural Networks** (e.g., **LSTMs**) to find a better fit for the data.

---

### **Relevant Graphs**

<img width="1005" height="634" alt="image" src="https://github.com/user-attachments/assets/f533c2d3-cb23-47a6-814f-4060c4ffbf25" />
