# flight-delay-prediction
Regression analysis predicting airline delays using Python and Scikit-Learn.
# ✈️ Flight Delay Prediction (Regression Analysis)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

## 📌 Project Overview
This project applies **Supervised Machine Learning (Regression)** to predict the total minutes of delay for airline flights. By analyzing historical flight data, we identify key drivers of delays—specifically focusing on **flight volume** and **airline carriers**.

The model achieves high accuracy by using **One-Hot Encoding** to handle categorical airline data and **Linear Regression** to quantify the relationship between flight traffic and delay time.

---

## 🔍 Key Features
* **Data Cleaning:** Handled missing values and filtered dataset to relevant operational metrics.
* **Feature Engineering:** Applied **One-Hot Encoding** to convert categorical `carrier` text data (e.g., "Southwest", "Delta") into numerical format for the model.
* **Predictive Modeling:** Built a **Linear Regression** model to predict continuous delay times.
* **Performance Analysis:** Evaluated model using R-Squared and Mean Absolute Error (MAE).

---

## 📊 Model Performance
The model demonstrates an exceptionally strong fit for the data.

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **R-Squared ($R^2$)** | **0.95 (95.3%)** | The model explains 95% of the variance in flight delays. This confirms a strong linear relationship: **More Flights = More Delays**. |
| **Mean Absolute Error (MAE)** | **~951 minutes** | On a monthly aggregate scale where delays often exceed 100,000 minutes, this represents an error rate of **<1%**. |

### 💡 Key Insight
The analysis confirms that **Airline Carrier** and **Flight Volume** are nearly perfect predictors of total delay time on a macro scale. While individual outlier flights may deviate, the aggregate trend is highly predictable.

---

## 🛠️ Tech Stack
* **Python**: Core programming language.
* **Pandas**: For data manipulation and aggregation.
* **Scikit-Learn**: For training the Linear Regression model.
* **Seaborn / Matplotlib**: For visualizing delay distributions and correlations.

---

## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/flight-delay-prediction.git](https://github.com/yourusername/flight-delay-prediction.git)
