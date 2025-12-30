# Canadian Business Risk Analysis

Sector-Level Insolvency Risk Classification & Dashboard

📌 Project Overview

This project analyzes sector-level business risk in Canada by combining historical insolvency data with macroeconomic indicators.
Using machine learning, sectors are classified into Low, Medium, and High Risk categories, and results are presented through an interactive Power BI dashboard for decision-making and policy analysis.

The objective is not to forecast exact insolvency counts, but to identify structurally vulnerable sectors based on learned patterns from historical data.

🎯 Key Objectives

Identify high-risk Canadian business sectors

Quantify risk probability at the sector level

Classify sectors into Low / Medium / High Risk

Visualize insights through a professional dashboard

Support risk-aware planning for policymakers, lenders, and analysts

🧠 Methodology

1️⃣ Data Collection & Integration

Multiple datasets were merged to capture both business outcomes and economic conditions:

- Sector-wise insolvency counts

- GDP and GDP growth metrics

- CPI and inflation indicators

- Volatility measures

- Lagged insolvency features

- Industry classification (sector codes)

All datasets were aligned temporally and by sector to ensure consistency.

2️⃣ Data Preprocessing

To prepare the data for modeling:

- Handled missing values and inconsistencies

- Engineered lagged and volatility features

- Encoded sector information numerically

- Standardized final feature set for modeling

- The output of this stage was a clean, model-ready dataset.

3️⃣ Risk Modeling (Classification Approach)

Instead of predicting exact insolvency counts, the problem was reframed as a risk classification task.

Why classification?

- Insolvency counts are noisy and volatile

- Stakeholders care more about risk exposure than exact numbers

- Classification provides actionable insight

Model Used

Random Forest Classifier

Chosen for:

- Non-linear pattern capture

- Robustness on small datasets

- Interpretability via feature importance

- Probability outputs

4️⃣ Risk Probability Estimation

For each sector-period observation, the model outputs:

P(High Risk)


This probability reflects the model’s confidence that a sector is structurally risky.

Key derived metrics:

- Risk Probability – model confidence for High Risk

- Predicted Risk – binary label based on probability threshold

- High-Risk Rate – frequency of high-risk classification per sector

- Average Risk Probability – mean risk confidence per sector

5️⃣ Sector-Level Risk Aggregation

Sector-level risk scores were computed by aggregating model outputs:

Metric	Meaning:

- Avg Risk Probability	Model confidence of sector risk
- High Risk Rate	Frequency of high-risk classification
- Avg Insolvencies	Historical severity indicator
- Risk Label	Low / Medium / High Risk

Risk labels were assigned using probability bands:

- Low Risk: < 0.40

- Medium Risk: 0.40 – 0.70

- High Risk: > 0.70

📊 Dashboard & Visualization (Power BI)

An interactive Power BI dashboard was built to communicate results clearly.

Dashboard Features

🔹 KPI Cards

- Total number of sectors

- Count of high-risk sectors

- High-risk sector share (%)

- Average risk probability

- Average insolvencies

🔹 Sector Risk Ranking

- Horizontal bar chart ranking sectors by average risk probability

- Color-coded by risk category

🔹 Risk Category Distribution

- Donut chart showing Low / Medium / High risk composition

🔹 Risk vs Severity Analysis

  Scatter plot:

- X-axis: Avg Risk Probability

- Y-axis: Avg Insolvencies

- Color: Risk Category

- Identifies high-confidence, high-impact sectors

🔹 Interactive Filters

- Sector selector

- Risk category slicer


📈 Key Insights

- Several service-oriented and cyclical sectors exhibit consistently high risk probabilities

- High risk does not always imply high insolvency counts, highlighting structural vulnerability

- Certain sectors remain resilient despite macroeconomic volatility

- Risk probability provides a more stable indicator than raw insolvency counts

🛠️ Tech Stack

Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)

Random Forest Classification

Power BI (DAX, interactive dashboards)

Jupyter Notebooks

🚀 Use Cases

- Financial risk assessment

- Credit policy evaluation

- Economic research
