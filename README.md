# Cardamom-Price-Predictor (CardaPredict-AI) 🌿

## What is this Project?
This project is an advanced **Time-Series Forecasting System** specifically designed to predict the price of **Indian Cardamom**. It solves the problem of market price volatility by merging two different worlds of data:
1. **Financial/Market Data:** Historical auction prices and quantities sold.
2. **Environmental Data:** Detailed weather patterns (Rainfall, Soil Moisture, Temp) from India’s cardamom-growing regions.

The goal is to provide a **14-day future price forecast** to help farmers and traders make data-backed decisions.

---

## The Hybrid Brain (Algorithms)
The system doesn't rely on one model; it uses a **Hybrid Ensemble Approach** to ensure the highest accuracy:

1. **CNN-LSTM (Deep Learning):**
   - **CNN:** Extracts hidden "spatial" patterns in the price movement.
   - **LSTM:** Remembers "long-term" seasonal trends and cycles.
2. **XGBoost (Machine Learning):**
   - Handles tabular data perfectly and calculates the impact of weather variables (like rainfall) on the final price.

---

##  Performance & Error Rates (Accuracy)
Based on the final evaluation in the notebooks, the models achieved the following results:

### 1. XGBoost Model Performance:
- **RMSE (Root Mean Squared Error):** `17.81 Rs/Kg`
- **MAE (Mean Absolute Error):** `14.03 Rs/Kg`
*This model shows exceptional performance in handling non-linear tabular features.*

### 2. Final Ensemble Model (Overall Forecast):
- **Final RMSE:** `34.21 Rs/Kg`
*The ensemble maintains a robust balance between the Deep Learning predictions and XGBoost, providing a reliable 14-day trend.*

---

##  Data Pipeline Highlights
- **The Critical Fix:** Handled missing data during market holidays and lockdowns using advanced time-series interpolation.
- **Feature Engineering:** - **Price Momentum:** Tracks the "speed" of price changes.
    - **Lag Features:** Uses the last 30 days of data to predict the next 14.
    - **Weather Integration:** Incorporates `Soil Moisture` and `Precipitation` as leading indicators for price shifts.

---

##  How the Files are Organized
- `Data_Preprocessing_Cardmom.ipynb`: Where the raw data is cleaned, merged, and prepared.
- `Modle_XGB_LSTM.ipynb`: The core training notebook containing the CNN-LSTM architecture and XGBoost ensemble.
- `India_Cardamom_Final_Ready.csv`: The final "Gold" dataset ready for AI training.

---

##  How to Run
1. Clone the repo.
2. Ensure you have `TensorFlow`, `XGBoost`, and `Pandas` installed.
3. Run `Modle_XGB_LSTM.ipynb` to see the 14-day forecast visualization.
