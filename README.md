# Stock_Price_Predictor

A machine learning project to predict stock price movements using historical Tesla stock data. This project implements multiple classification models to predict whether the stock price will go up or down.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Models Used](#models-used)
- [Results](#results)
- [Data Processing](#data-processing)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project predicts Tesla stock price movements using machine learning classification algorithms. By analyzing historical price data, volume trends, and temporal features, the model predicts whether the stock price will increase or decrease.

**Key Objective:** Build an accurate classification model to predict stock price movements based on historical data.

## ✨ Features

- **Data Analysis & Visualization:** Comprehensive exploratory data analysis (EDA) with distribution plots and time-series visualization
- **Feature Engineering:** Extraction of temporal features (day, month, year) from date columns
- **Data Preprocessing:** Feature scaling using StandardScaler for optimal model performance
- **Multiple Models:** Implementation of three different ML algorithms for comparison
- **Model Evaluation:** Performance metrics including accuracy, precision, recall, and F1-score

## 📊 Dataset

**Source:** Tesla.csv (Historical Tesla Stock Data)

**Dataset Statistics:**
- **Total Records:** 1,692 rows
- **Time Period:** Historical Tesla stock data
- **Features:**
  - `Date`: Trading date
  - `Open`: Opening price
  - `High`: Highest price of the day
  - `Low`: Lowest price of the day
  - `Close`: Closing price
  - `Volume`: Trading volume
  - `Adj Close`: Adjusted closing price

**Data Preprocessing:**
- Removed redundant 'Adj Close' column (identical to 'Close')
- Extracted temporal features (day, month, year) from date
- Applied StandardScaler for feature normalization

## 📁 Project Structure

```
Stock_Price_Predictor/
├── Stock_Price_Predictor.ipynb    # Main Jupyter notebook with complete analysis
├── Tesla.csv                       # Historical Tesla stock data
├── README.md                       # Project documentation
└── requirements.txt                # Python dependencies (optional)
```

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab

### Required Libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
```

Or install from requirements file:
```bash
pip install -r requirements.txt
```

### Required Packages
- **NumPy:** Numerical computations
- **Pandas:** Data manipulation and analysis
- **Matplotlib & Seaborn:** Data visualization
- **Scikit-learn:** Machine learning algorithms and preprocessing
- **XGBoost:** Gradient boosting classifier

## 💻 Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Suprasiddh/Stock_Price_Predictor.git
   cd Stock_Price_Predictor
   ```

2. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook Stock_Price_Predictor.ipynb
   ```

3. **Run the notebook cells in order:**
   - Import required libraries
   - Load Tesla.csv dataset
   - Perform exploratory data analysis
   - Preprocess and scale features
   - Train machine learning models
   - Evaluate model performance

## 🤖 Models Used

The project implements and compares three different classification algorithms:

### 1. **Logistic Regression**
- Simple and interpretable linear classification model
- Good baseline for binary classification
- Fast training and prediction

### 2. **Support Vector Machine (SVC)**
- Powerful non-linear classifier
- Effective for high-dimensional data
- Uses kernel tricks for complex decision boundaries

### 3. **XGBoost Classifier**
- Gradient boosting ensemble method
- Handles non-linear relationships well
- Often provides the best performance
- Robust to outliers and missing values

## 📈 Results

The models are evaluated using standard classification metrics:
- **Accuracy:** Overall correctness of predictions
- **Precision:** True positives among predicted positives
- **Recall:** True positives among actual positives
- **F1-Score:** Harmonic mean of precision and recall
- **Confusion Matrix:** Detailed breakdown of predictions

*Note: Specific results can be viewed by running the notebook and examining the evaluation metrics.*

## 🔧 Data Processing Steps

1. **Data Loading:** Import Tesla.csv into a Pandas DataFrame
2. **Exploratory Analysis:**
   - Display dataset shape and basic statistics
   - Analyze data types and missing values
   - Create distribution plots for price and volume
   - Generate box plots for outlier detection

3. **Feature Engineering:**
   - Extract day, month, year from date column
   - Drop redundant columns

4. **Data Scaling:**
   - Apply StandardScaler to normalize features
   - Ensure all features are on the same scale

5. **Train-Test Split:**
   - Divide data into training and testing sets
   - Maintain data balance for fair evaluation

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch:**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes and commit:**
   ```bash
   git commit -m "Add your descriptive message"
   ```
4. **Push to your fork:**
   ```bash
   git push origin feature/your-feature-name
   ```
5. **Create a Pull Request with detailed description**

### Suggestions for Improvement:
- Add additional technical indicators (RSI, MACD, Bollinger Bands)
- Implement LSTM/RNN models for time-series prediction
- Add real-time stock prediction capability
- Create a web interface for predictions
- Test with other stock symbols
- Optimize hyperparameters using GridSearchCV or RandomizedSearchCV

## 📝 License

This project is open source and available under the MIT License.

## 📞 Contact

For questions or suggestions, please open an issue on GitHub or contact the project maintainer.

---

**Happy Predicting! 🚀**

*Last Updated: 2026*
