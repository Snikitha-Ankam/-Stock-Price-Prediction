# 📊 Tesla Stock Price Direction Prediction

This project uses **Machine Learning** techniques to predict the **direction of Tesla's stock price movement (Up/Down)** based on historical stock market data and engineered features. The objective is to determine whether the **next day's closing price** will be higher than the current day's closing price.

---

## 🎯 Project Objective

Stock market prediction is a challenging problem due to market volatility and numerous influencing factors. This project focuses on predicting the **direction of Tesla (TSLA) stock price movement** using classification algorithms and feature engineering techniques.

---

## 📁 Dataset

The dataset consists of historical Tesla stock market data stored in a CSV file containing the following features:

| Feature | Description |
|-----------|-------------|
| Date | Trading date |
| Open | Opening stock price |
| High | Highest stock price of the day |
| Low | Lowest stock price of the day |
| Close | Closing stock price |
| Adj Close | Adjusted closing price |
| Volume | Number of shares traded |

### Target Variable

The target variable is defined as:

- **1 (Up)** → Next day's closing price is higher than today's closing price.
- **0 (Down)** → Next day's closing price is lower than or equal to today's closing price.

---

## 🧪 Feature Engineering

To improve model performance, the following features were created:

### 1. Open-Close Difference

```python
open_close = Open - Close
```

Measures the difference between the opening and closing prices.

### 2. Low-High Difference

```python
low_high = Low - High
```

Captures the daily price range.

### 3. Quarter-End Indicator

```python
is_quarter_end = 1 if month in [3, 6, 9, 12] else 0
```

Indicates whether the trading day falls at the end of a financial quarter.

---

## 🧠 Machine Learning Models

The following classification algorithms were trained and evaluated:

### Logistic Regression

- Simple and interpretable linear classifier.
- Used as the primary prediction model.

### Support Vector Machine (Polynomial Kernel)

- Captures nonlinear relationships in the data.
- Uses a polynomial kernel for classification.

### Random Forest Classifier

- Ensemble learning method.
- Combines multiple decision trees to improve prediction accuracy.

---

## 📊 Model Evaluation Metrics

The models were evaluated using the following metrics:

### Accuracy

Measures the percentage of correctly classified instances.

```text
Accuracy = Correct Predictions / Total Predictions
```

### F1 Score

Balances precision and recall.

```text
F1 Score = 2 × (Precision × Recall) / (Precision + Recall)
```

### Log Loss

Measures the uncertainty of predictions.

```text
Lower Log Loss = Better Performance
```

---

## 📈 Data Visualization

Several visualizations were created to better understand the dataset:

### Stock Price Trend

- Visualizes Tesla stock price movement over time.

### Distribution Plots

- Shows the distribution of numerical features.

### Box Plots

- Identifies outliers and feature spread.

### Correlation Heatmap

- Displays relationships between variables.

### Target Distribution

- Shows the balance between upward and downward stock movements.

---

## 🚀 Prediction on New Data

The trained **Logistic Regression model** is used to predict whether Tesla's stock price will move upward or downward.

### Example Input

```python
new_data = [[open_close, low_high, is_quarter_end]]
```

### Prediction Output

```text
Prediction: Stock Price Will Go Up 📈
```

or

```text
Prediction: Stock Price Will Go Down 📉
```

### Confidence Message

The model also provides a confidence score indicating the certainty of the prediction:

```text
Confidence: 87.5%
```

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📂 Project Structure

```text
Tesla-Stock-Prediction/
│
├── data/
│   └── TSLA.csv
│
├── notebooks/
│   └── Tesla_Stock_Prediction.ipynb
│
├── models/
│   └── logistic_regression_model.pkl
│
├── images/
│   ├── price_trend.png
│   ├── heatmap.png
│   └── target_distribution.png
│
├── requirements.txt
├── README.md
└── app.py
```

---

## ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/tesla-stock-price-direction-prediction.git
```

2. Navigate to the project directory:

```bash
cd tesla-stock-price-direction-prediction
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run the project:

```bash
python app.py
```

---

## 📌 Future Improvements

- Incorporate technical indicators (RSI, MACD, Moving Averages)
- Use deep learning models such as LSTM
- Include market sentiment analysis from news and social media
- Deploy as a web application using Streamlit or Flask

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

Developed as a Machine Learning project for stock market trend prediction using Tesla stock data.
