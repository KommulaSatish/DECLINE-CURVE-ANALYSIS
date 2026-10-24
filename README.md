# Decline Curve Analysis (DCA) of an Oil Well

**A Python-based petroleum engineering project for production decline modeling, well performance evaluation, production forecasting, and Estimated Ultimate Recovery (EUR) estimation.**

---

## 📌 Project Overview

This project applies **Arps Decline Curve Analysis (DCA)** to historical oil well production data to evaluate production performance, compare decline models, forecast future oil production, estimate productive well life, and calculate Estimated Ultimate Recovery (EUR).

The complete workflow was implemented in **Python using Jupyter Notebook**, combining petroleum engineering principles with numerical optimization, statistical model evaluation, and production data visualization.

> **Data Confidentiality:** The original production dataset is not included in this repository due to confidentiality requirements.

## 🎯 Project Objectives

- Analyze historical oil well production performance.
- Implement **Exponential, Hyperbolic, and Harmonic** decline models.
- Estimate decline parameters using nonlinear regression.
- Compare model performance using statistical metrics.
- Forecast future oil production up to the specified economic limit.
- Estimate cumulative production and Estimated Ultimate Recovery (EUR).
- Visualize historical production, forecasts, and yearly production trends.

## 🛠️ Technologies Used

| Category | Tools |
|---|---|
| Programming Language | Python |
| Development Environment | Jupyter Notebook |
| Data Analysis | Pandas, NumPy |
| Scientific Computing | SciPy |
| Data Visualization | Matplotlib |
| Numerical Optimization | `scipy.optimize.curve_fit` |

## 📂 Input Data

The analysis uses historical monthly production data containing the following variables:

- **Production Time:** Time elapsed during the production history.
- **Oil Production Rate:** Monthly oil production rate used for decline modeling.
- **Water Cut:** Fraction of produced liquid volume contributed by water.
- **Gas-Oil Ratio (GOR):** Ratio of produced gas volume to produced oil volume.

The dataset is proprietary and has therefore been excluded from this public repository.

## ⚙️ Methodology

### 1. Historical Production Analysis

Production data was organized and analyzed using Pandas to understand the well's historical performance. The analysis included oil production rate, water cut, and gas-oil ratio trends over time.

### 2. Arps Decline Curve Modeling

Three classical decline models were implemented to characterize the decline in oil production.

| Decline Model | Description |
|---|---|
| **Exponential** | Assumes a constant nominal decline rate. |
| **Hyperbolic** | Represents a changing decline rate using a hyperbolic exponent. |
| **Harmonic** | A special case of hyperbolic decline with a decline exponent of \(b=1\). |

### 3. Parameter Estimation

Nonlinear least-squares regression using `scipy.optimize.curve_fit` was applied to estimate the model parameters.

The estimated parameters include:

- **Initial Production Rate (\(q_i\))** — the production rate at the beginning of the modeled decline period.
- **Initial Nominal Decline Rate (\(D_i\))** — the initial rate of production decline.
- **Hyperbolic Exponent (\(b\))** — a parameter controlling the shape of the hyperbolic decline curve.

Parameter bounds were applied to help obtain physically meaningful solutions.

### 4. Model Evaluation

The decline models were evaluated using statistical performance metrics.

- **Coefficient of Determination (\(R^2\))** — measures how well the model explains the observed variation in production.
- **Root Mean Square Error (RMSE)** — measures the typical magnitude of prediction errors in the production-rate units.

The models were compared using these metrics to identify the best-fitting model for the analyzed production history.

### 5. Production Forecasting

The fitted decline models were used to forecast future oil production. Forecasting was continued up to the specified economic production limit, subject to the assumptions and constraints implemented in the notebook.

### 6. Cumulative Production and EUR Estimation

The analysis included:

- Historical cumulative oil production.
- Forecast cumulative oil production.
- Estimated Ultimate Recovery (EUR), based on historical cumulative production and forecast production through the defined economic limit.

### 7. Yearly Production Analysis

Monthly production data and forecasts were used to generate yearly production summaries, including:

- Yearly average oil production rate.
- Yearly oil production.
- Yearly cumulative oil production.

## 📊 Engineering Analysis and Visualizations

The project includes the following analyses and plots:

- Historical oil production rate versus time.
- Water cut versus time.
- Gas-oil ratio versus time.
- Exponential decline curve fitting.
- Hyperbolic decline curve fitting.
- Harmonic decline curve fitting.
- Comparison of decline model performance.
- Historical and forecast production profiles.
- Production forecast up to the economic limit.
- Historical and forecast cumulative production.
- Yearly average production rate.
- Yearly oil production and cumulative production trends.

## 🧮 Model Comparison Parameters

The decline models are compared using the following parameters and metrics.

| Parameter | Purpose |
|---|---|
| \(q_i\) | Initial production rate |
| \(D_i\) | Initial nominal decline rate |
| \(b\) | Hyperbolic decline exponent |
| \(R^2\) | Goodness-of-fit assessment |
| RMSE | Prediction error assessment |

The best-fitting statistical model is not automatically the best engineering forecast. Forecast reliability also depends on production history, model assumptions, operating conditions, and the selected economic limit.

## 💡 Key Petroleum Engineering Concepts Demonstrated

- Decline Curve Analysis (DCA).
- Reservoir and well production performance evaluation.
- Arps exponential, hyperbolic, and harmonic decline models.
- Production forecasting and economic-limit analysis.
- Cumulative production and Estimated Ultimate Recovery (EUR).
- Nonlinear regression and decline parameter estimation.
- Statistical model comparison and error analysis.
- Yearly production trend analysis.

## 🧑‍💻 Technical Skills Demonstrated

**Petroleum Engineering:** Decline Curve Analysis, production performance evaluation, production forecasting, and EUR estimation.

**Python and Data Analytics:** Pandas, NumPy, SciPy, Matplotlib, data processing, nonlinear curve fitting, and scientific visualization.

**Engineering Interpretation:** Decline model comparison, parameter interpretation, forecast analysis, and technical reporting.

## 📁 Repository Structure

```text
DECLINE-CURVE-ANALYSIS/
│
├── DCA.ipynb
└── README.md
```

- `DCA.ipynb` — Jupyter Notebook containing the Python implementation, decline models, analysis workflow, and visualizations.
- `README.md` — Project documentation, methodology, tools, and engineering scope.

## 🔒 Confidentiality and Data Protection

This repository is intended to demonstrate the engineering methodology and Python implementation of Decline Curve Analysis for educational and portfolio purposes.

To comply with confidentiality requirements:

- The original production dataset is not included.
- Proprietary reservoir data, field names, well identifiers, and internal company documents are not shared.
- Notebook outputs containing confidential production information have been removed before publication.

## 🚀 Project Purpose

This project demonstrates how **petroleum engineering knowledge and Python-based data analysis can be combined** to evaluate production decline, compare forecasting models, and estimate recoverable production within a defined economic limit.

The workflow provides a foundation for further work in production surveillance, reservoir performance analysis, and data-driven petroleum engineering.
