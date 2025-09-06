# 📈 Stock Price Prediction using LSTM

This project predicts **stock prices** using a **Long Short-Term Memory (LSTM) deep learning model**.  
It fetches stock data (e.g., Reliance Industries) with **yFinance**, preprocesses it, and trains an LSTM model to predict **Open, High, Low, Close, and Volume**.

---

## 📌 Features
- Fetch stock data with **yFinance**
- Store data as CSV for further analysis
- Preprocessing:
  - Normalization using **MinMaxScaler**
  - Sequence creation for time-series forecasting (60-day lookback)
- LSTM Model:
  - Built with **Keras/TensorFlow**
  - Trained on OHLCV features
- Evaluation:
  - Predictions compared with actual values
  - Visualization of **Actual vs Predicted** for each feature

---

## 📂 Project Structure
```
├── Get_Stock_Data.ipynb       # Fetch and save stock data
├── Stock_Price_Predict.ipynb  # Train & evaluate LSTM model
├── RELIANCE_StockData.csv     # Example dataset (generated)
├── README.md                  # Documentation
```

---

## ⚙️ Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/StockPricePrediction.git
   cd StockPricePrediction
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib tensorflow yfinance
   ```

3. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

---

## 🚀 Usage

### Step 1: Fetch Stock Data
Run `Get_Stock_Data.ipynb` to download stock data (example: Reliance Industries):
```python
import yfinance as yf

df = yf.download("RELIANCE.NS", start="2023-01-01", end="2025-08-08")
df.to_csv("RELIANCE_StockData.csv")
```

### Step 2: Train Prediction Model
Run `Stock_Price_Predict.ipynb`:
- Loads `RELIANCE_StockData.csv`
- Preprocesses & scales data
- Trains LSTM model
- Predicts and visualizes results

---

## 📊 Example Output
- Visualization of **Actual vs Predicted** prices:
  - Open
  - High
  - Low
  - Close
  - Volume

---

## 📈 Results
- Successfully predicted **short-term stock price patterns** using LSTM.  
- Captured trends in OHLC values with reasonable accuracy.  
- Prediction visualizations show close alignment with actual data.  

---

## 🛠️ Technologies Used
- Python 🐍  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow/Keras  
- Matplotlib  
- yFinance  

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
