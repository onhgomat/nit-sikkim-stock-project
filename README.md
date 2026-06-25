# 📈 Stock Market Trend Prediction using Machine Learning and Deep Learning

## Overview

This project implements a comprehensive stock market trend prediction system using Machine Learning, Ensemble Learning, Feature Selection, and Deep Learning techniques.

The objective is to predict the next-day stock price movement (Up/Down) using technical indicators, market features, lag variables, and historical stock data collected from 1996–2026.

The project compares traditional machine learning models with deep learning architectures to evaluate their effectiveness in financial time-series forecasting.

---

## Features

### Data Processing

* Historical stock market data analysis
* Technical indicator generation
* Missing value handling
* Feature engineering
* Time-series aware train-test splitting

### Feature Engineering

* Moving Averages (MA5, MA20, MA50)
* Exponential Moving Averages (EMA12, EMA26)
* MACD and Signal Line
* Bollinger Bands
* Relative Strength Index (RSI)
* Momentum Indicators
* Volatility Measures
* Lag Features
* Volume-Based Features
* NIFTY Market Features
* Market Event Features

### Feature Selection

* Particle Swarm Optimization (PSO)
* Automated feature subset selection
* Reduced dimensionality
* Improved model efficiency

### Machine Learning Models

* Linear Regression
* XGBoost Classifier
* CatBoost Classifier

### Deep Learning Models

* LSTM (Long Short-Term Memory)
* GRU (Gated Recurrent Unit)
* Transformer-based Architecture

---

## Dataset

### Input Features

The dataset contains 59 columns including:

* Open
* High
* Low
* Close
* Volume
* Returns
* Technical Indicators
* Market Indicators
* Lag Features
* Economic Event Features

### Target Variable

Binary Classification:

* 1 → Stock Price Increases Next Day
* 0 → Stock Price Decreases Next Day

---

## Project Structure

```text
stock_ml_pipeline/
│
├── data/
│   └── stock_data.xlsx
│
├── src/
│   ├── data_loader.py
│   ├── preprocess.py
│   ├── train_regression.py
│   ├── train_xgboost.py
│   ├── train_catboost.py
│   ├── train_transformer.py
│   ├── pso_feature_selection.py
│   └── evaluate.py
│
├── src_dl/
│   ├── data_sequence.py
│   ├── train_lstm.py
│   └── train_gru.py
│
├── main.py
├── dl_main.py
├── requirements.txt
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/stock-market-prediction.git

cd stock-market-prediction
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Running Machine Learning Pipeline

```bash
python main.py
```

Models executed:

* Regression Model
* XGBoost
* CatBoost
* PSO Feature Selection

---

## Running Deep Learning Pipeline

### LSTM

```bash
python dl_main.py
```

### GRU

Update import in:

```python
from src_dl.train_gru import train_gru
```

Then run:

```bash
python dl_main.py
```

---

## Experimental Results

### Machine Learning Results

| Model    | Accuracy |
| -------- | -------- |
| XGBoost  | 69.17%   |
| CatBoost | 69.08%   |

### Deep Learning Results

| Model       | Accuracy    |
| ----------- | ----------- |
| Transformer | ~50%        |
| LSTM        | ~50%        |
| GRU         | In Progress |

---

## Key Findings

* Ensemble models significantly outperformed deep learning architectures.
* XGBoost achieved the highest classification accuracy.
* CatBoost produced comparable performance.
* LSTM and Transformer models showed overfitting and poor generalization.
* Feature engineering contributed more to performance gains than sequence modeling.

---

## Technologies Used

### Programming Language

* Python

### Machine Learning

* Scikit-Learn
* XGBoost
* CatBoost

### Deep Learning

* PyTorch

### Data Analysis

* Pandas
* NumPy

### Visualization

* Matplotlib
* Seaborn

### Optimization

* Particle Swarm Optimization (PSO)

---

## Future Work

* Bidirectional GRU
* CNN-LSTM Hybrid
* Temporal Fusion Transformer (TFT)
* Attention-based Forecasting Models
* Hyperparameter Optimization
* Explainable AI using SHAP and LIME
* Real-time Prediction Dashboard
* Deployment using Streamlit or Flask

---

## Author

**Tamoghno Ghosh**

B.Tech CSE Student
Institute of Engineering & Management (IEM), Kolkata

---

## License

This project is released under the MIT License.

Feel free to use, modify, and distribute this project for academic and research purposes.
