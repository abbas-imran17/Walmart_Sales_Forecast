📈 Walmart Sales Forecasting App

An interactive time series forecasting project built with:

Facebook Prophet for forecasting

Streamlit for a modern web interface

Plotly for dynamic visualizations

Cross-validation for evaluating forecast accuracy

Upload any CSV with Date and Weekly_Sales, and the app will forecast future values and generate visual insights instantly.

🚀 Features

✔ Upload your own sales dataset (CSV)
✔ Auto-convert date column & clean the data
✔ Visualize historical sales
✔ Train a Prophet model in real-time
✔ Forecast daily/weekly/monthly values
✔ Interactive forecast plots using Plotly
✔ Trend, weekly, and yearly component analysis
✔ Cross-validation (MAPE, MAE, RMSE, etc.)
✔ Download forecast results as CSV

📁 Project Structure
│── app.py                     # Streamlit application
│── prophet_forecast.py        # Prophet training & evaluation
│── Walmart_Sales.csv          # Sample dataset
│── README.md                  # Documentation
│── requirements.txt           # Dependencies

🛠️ Requirements

Install all dependencies:

pip install streamlit prophet plotly pandas matplotlib


If Prophet fails to install, use:

pip install prophet --no-build-isolation

▶️ How to Run the App
1️⃣ Run locally
streamlit run app.py


The app will open automatically in your browser.

📂 Data Format

Your CSV must contain:

Column	Description
Date	Date of sale (DD-MM-YYYY or YYYY-MM-DD)
Weekly_Sales	Sales value for that date/week

Example:

Date,Weekly_Sales
05-01-2023,20500
12-01-2023,19900
19-01-2023,21500

📉 Forecasting Options

In the sidebar:

Frequency Options

Days → D

Weeks → W

Months → M

Horizon

Choose how many future periods to forecast.

📊 Model Evaluation (Cross-Validation)

The app performs:

Rolling forecast origin CV

365-day training window

180-day steps

60-day horizon

Generates metrics like:

MAPE (Mean Absolute Percentage Error)

MAE

RMSE

Coverage

And shows a Plotly MAPE curve.

📥 Download Results

Download your forecast as a CSV file directly from the app:

ds, yhat, yhat_lower, yhat_upper


Easy for Excel, Power BI, or further ML pipelines.

🛠️ Customization

You can modify:

Trend/seasonality settings

Add holidays

Add regressors

Change forecast horizons

Customize visual themes

🧪 Future Improvements

ARIMA / LSTM comparison tab

Auto hyperparameter tuning

Multiple store forecasting

Prophet holidays + promo calendar

Deploy on Streamlit Cloud or AWS

🤝 Contributions

Pull requests are welcome!
For major changes, open an issue first.

📜 License

MIT License
