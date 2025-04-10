# Shipment Volume Prediction

A project for predicting the **daily shipment volume** based on calendar attributes, weather conditions, and forecasts from client X.

---

## Project Overview

The objective was to build a regression model capable of forecasting the number of shipments for a given day. The model with the best performance was **XGBoost Regressor**, which achieved the lowest RMSE and MAE.

---

## Data Sources

### 1. `DimDates`
Detailed calendar data (2020–2023), including:
- Public holidays and weekends,
- Courier billing periods,
- Weekday/month names in Polish and English.

### 2. `PostingVolume`
Daily shipment volumes (2021-01-01 to 2023-08-31), categorized by:
- Product: `APM`, `COURIER`
- Customer: `X`, `Rest` (other clients)

### 3. `Clients_Orders`
Monthly shipment forecasts provided by client X (only available for 2023).

### 4. `Zadanie_Dane_Temperatura`
Daily weather data from **Warsaw** and **Kraków**:
- Max / min / average temperature,
- Precipitation (mm),
- Snow cover (cm).

---

## Project Structure

### 1. Initial Data Analysis
- Summary statistics, null value analysis, outlier detection,
- Consistency checks in categorical fields and date conversions.

### 2. Data Processing
- Handling missing values and data errors (e.g. negative volumes),
- Aggregation and merging of datasets into `combined_df`.

### 3. Exploratory Data Analysis (EDA)
- Seasonal trends by **month**, **weekday**, **holiday**,
- Shipment pattern differences between client X and other clients,
- Evaluation of **client forecast accuracy**,
- Analysis of **weather impact** on shipment volumes.

### 4. Modeling
- Feature selection based on correlation analysis,
- Feature scaling,
- Model comparison:
  - Decision Tree Regressor  
  - Linear Regression  
  - Random Forest Regressor  
  - **XGBoost Regressor**
  - KNeighbors Regressor  

### 5. Evaluation
- Best MAE: `74,198`
- Best RMSE: `97,654`
- Visualizations: actual vs predicted volume (line and scatter plots).

---

## Technologies Used

- **Languages & Libraries**: Python, Pandas, NumPy, Scikit-learn, XGBoost
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Data formats**: CSV, Parquet, Excel

---

