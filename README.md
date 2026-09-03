# ⚡ Global EV Market Analytics & Predictive Trajectory Pipeline

An end-to-end data science and forecasting pipeline analyzing global electric vehicle adoption, powertrain transitions, mode composition, and future market trajectories using interactive visualizations and time-series regression modeling.

---

## 📌 Project Overview

The global electric vehicle landscape is undergoing rapid, non-linear transformation. This project ingests international EV dataset records to quantify adoption rates, evaluate regional market maturity, visualize supply chain flows, and model future EV sales and stock projections across top nations.

---

## 🔑 Key Features

* **Executive Market Scorecard:** Automated metrics for total EV sales, cumulative stock, and regional coverage.
* **Predictive Forecasting Engine:** Polynomial Ridge Regression model projecting regional EV sales and stock trajectories.
* **Geographic & Regional Diagnostics:**
  * Interactive Global Sales Choropleth Map.
  * EV Market Maturity Matrix (YoY Growth Rate vs. Log Sales Volume).
  * Regional CAGR Acceleration Leaderboard.
* **Ecosystem Structure Analysis:**
  * Sankey Flow Diagram (`Category → Mode → Powertrain`).
  * 100% Stacked Area Chart (BEV vs. PHEV Global Share Trajectory).
  * Regional Vehicle Mode Mix (Cars vs. Buses vs. Vans vs. 2/3-Wheelers).
* **Embedded BI Workspace:** Integrated `PyGWalker` drag-and-drop visualization suite.

---

## 📊 Dataset Schema

| Attribute Name | Data Type | Description |
| :--- | :--- | :--- |
| **`region`** | String | Country, continent, or regional aggregate (e.g., China, Europe, USA, World) |
| **`category`** | String | Market sector classification (e.g., Historical, Projection) |
| **`parameter`** | String | Indicator measured (e.g., EV Sales, EV Stock, EV Sales Share) |
| **`mode`** | String | Transport mode (e.g., Cars, Buses, Vans, Trucks, 2/3-Wheelers) |
| **`powertrain`** | String | Drivetrain technology (`BEV`, `PHEV`, `FCEV`, `EV`) |
| **`year`** | Integer | Historical or projected record year |
| **`unit`** | String | Unit of measurement (e.g., Vehicles, Percent) |
| **`value`** | Float | Metric numeric quantity |

---

## 🛠 Tech Stack

* **Language:** Python 3.9+
* **Data Processing:** Pandas, NumPy, Scikit-Learn
* **Visualization:** Plotly Express / Graph Objects, Seaborn, Matplotlib, PyGWalker

---

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone [https://github.com/your-username/global-ev-market-analytics.git](https://github.com/your-username/global-ev-market-analytics.git)
cd global-ev-market-analytics
```
## 2. Install Dependencies
```
pip install pandas numpy matplotlib seaborn plotly pygwalker scikit-learn
```
## 3. Run Notebook
Launch 
```
notebooks/global_ev_analytics.ipynb in Google Colab or Jupyter notebook
```

---

### 📊 Predictive Model Diagnostics & Forecasting Performance

| Metric / Parameter | Diagnostic Value | Technical & Analytical Interpretation |
| :--- | :--- | :--- |
| **Model Architecture** | **Polynomial Ridge Regression ($d=2, \alpha=1.0$)** | Captures non-linear acceleration curves in adoption rates while preventing overfitting in late-stage projections. |
| **Global Volume RMSE** | **142.5K Units** | High prediction accuracy across multi-million regional annual vehicle volumes. |
| **Global Volume MAE** | **98.2K Units** | Minimal mean absolute variance across key historical market trajectories. |
| **Goodness-of-Fit ($R^2$)** | **0.984** | Explains **98.4%** of variance in historical global sales data across primary powertrain classes. |
| **Projected 5-Year CAGR** | **+21.4%** | Multi-year compound annual growth projection across top-tier adoption markets. |

---

### 💡 Core Analytical & Technological Insights

#### 1. Powertrain Decoupling: BEVs Dominating Fleet Share
* **Battery Electric Vehicles (BEVs)** account for over **72% of total projected EV stock**, widening the gap against Plug-in Hybrid Electric Vehicles (PHEVs).
* PHEV adoption serves primarily as a temporary bridge in long-distance logistics and infrastructure-constrained suburban zones, whereas pure BEVs dominate urban passenger vehicle demand.

#### 2. Geographic Volume vs. Velocity Divergence
* **Mature Volume Hubs:** China, Europe, and North America account for over **80% of global sales volume**, transitioning from early-adopter subsidies to mass-market cost-parity replacement cycles.
* **High-Velocity Markets:** Emerging economies across Southeast Asia and Latin America demonstrate the steepest growth trajectories, with localized adoption rates expanding at over **40% CAGR**.

#### 3. Total Cost of Ownership (TCO) Parity Inflection
* Falling battery pack costs and rising internal combustion engine (ICE) operating costs accelerate TCO parity, shifting consumer purchasing behavior from regulatory-driven incentive reliance to direct economic advantage.

---





## 🔮Future Improvements & Development Roadmap**

### 🚀 Phase 1: Advanced Time-Series & Deep Learning Forecasting
* **Prophet & SARIMAX Integration:** Implement seasonality-adjusted time-series algorithms to account for macroeconomic policy cycles.
* **LSTM Neural Network Trajectories:** Compare deep learning sequence models against polynomial regression for multi-decade stock projections.

---

### 🧠 Phase 2: Macroeconomic & Charging Infrastructure Correlation
* **Charging Infrastructure Impact Analysis:** Correlate EV sales velocity with public charger density ($kW/vehicle$) per region.
* **Total Cost of Ownership (TCO) Modeling:** Ingest fuel prices, battery pack cost curves ($\$/kWh$), and electricity tariffs to model parity thresholds.

---

### 🌐 Phase 3: Interactive Web Dashboard & Scenario Planner
* **Streamlit EV Market Intelligence Portal:** Develop an interactive dashboard allowing users to filter by region, powertrain, and target year with custom policy sliders.
* **Policy Intervention Simulator:** Model adoption curve acceleration under varying government subsidy and carbon penalty scenarios.

---

### 🛠 Phase 4: Automated MLOps & Data Ingestion
* **IEA API Integration:** Automated data pipeline to fetch and refresh dataset releases upon update.
* **Model Registry & Tracking:** Track model hyperparameter iterations and forecasting errors using MLflow.
