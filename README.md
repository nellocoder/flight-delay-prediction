# ✈️ Flight Delay Prediction (Regression Analysis)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

## 📌 Project Overview
This project applies **Supervised Machine Learning (Regression)** to predict the total minutes of delay for airline flights. By analyzing historical flight data, we identify key drivers of delays, specifically focusing on **flight volume** and **airline carriers**.

The model achieves high accuracy by using **One-Hot Encoding** to handle categorical airline data and **Linear Regression** to quantify the relationship between flight traffic and delay time.

---

## 🔍 Key Features
* **Data Cleaning:** Handled missing values and filtered dataset to relevant operational metrics.
* **Feature Engineering:** Applied **One-Hot Encoding** to convert categorical `carrier` text data (e.g., "Southwest", "Delta") into numerical format for the model.
* **Predictive Modeling:** Built a **Linear Regression** model to predict continuous delay times.
* **Business Intelligence:** Visualized seasonality, airport bottlenecks, and airline efficiency metrics.
* **Hypothesis Testing:** Conducted a comparative analysis between Linear and Polynomial regression to test for non-linear congestion effects.

---

## 📈 Business Intelligence & Analytics

### 1. Seasonality Analysis (When to Fly?)
We analyzed average delay minutes across all 12 months to find the best travel windows.
* **Summer Peak (June/July):** A sharp spike in delays occurs here, likely driven by high vacation travel volume and summer thunderstorms.
* **Holiday Surge (December):** A secondary peak occurs in December, correlating with winter holiday travel and snowstorms.
* **The "Golden Window" (Sept/Nov):** The data shows a significant dip in delays during autumn, making this the most efficient time of year to fly.

### 2. Airport Bottlenecks (Where to Avoid?)
We identified the top 10 airports contributing the most to national delays.
* **The Hub Effect:** Major hubs like **Atlanta (ATL)**, **Chicago (ORD)**, and **Dallas (DFW)** consistently rank highest due to massive traffic volume.
* **Geographic Factors:** Coastal hubs like **San Francisco (SFO)** often appear due to weather volatility (fog) and congested airspace.

### 3. Airline Efficiency (The Fair Comparison)
Total delay minutes can be misleading because large airlines naturally have more delays. We normalized the data to calculate **Average Delay Minutes Per Flight**.
* **Result:** This metric reveals which airlines are truly inefficient per passenger trip, separating those who simply fly often from those who manage operations poorly.

---

## 📊 Model Performance (Champion Model)
The **Linear Regression** model (including Carrier data) demonstrates an exceptionally strong fit.

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **R-Squared ($R^2$)** | **0.95 (95.3%)** | The model explains 95% of the variance in flight delays. This confirms a strong linear relationship: **More Flights + Specific Carriers = More Delays**. |
| **Mean Absolute Error (MAE)** | **~951 minutes** | On a monthly aggregate scale where delays often exceed 100,000 minutes, this represents an error rate of **<1%**. |

---

## 🧪 Model Experimentation: Linear vs. Polynomial
We tested the hypothesis that delays might grow **exponentially** (rather than linearly) as flight volume increases (e.g., congestion collapse). We compared a Standard Linear Model against a Polynomial Model (Degree 2) using *only* flight volume.

| Model | R-Squared | Verdict |
| :--- | :--- | :--- |
| **Linear (Volume Only)** | **0.64** | **Winner.** The relationship is strictly linear. |
| **Polynomial (Degree 2)** | 0.60 | **Loser.** Adding complexity/curves introduced noise and reduced accuracy. |

**Key Findings:**
1.  **Linearity:** Delays accumulate steadily, not exponentially.
2.  **The "Carrier Effect":** Removing Carrier data dropped accuracy from **95%** to **64%**. This proves that **30% of delay variance** is driven by *who* is flying (operational efficiency), not just *how much* they are flying.

---

## 🛠️ Tech Stack
* **Python**: Core programming language.
* **Pandas**: For data manipulation and aggregation.
* **Scikit-Learn**: For training the Linear Regression and Polynomial Features.
* **Seaborn / Matplotlib**: For visualizing delay distributions and correlations.

---

## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/nellocoder/flight-delay-prediction.git](https://github.com/nellocoder/flight-delay-prediction.git)
