# 🎯 Project Objectives

The primary objective of this project is to develop an end-to-end predictive analytics framework capable of identifying loan segments that are likely to experience significant deterioration in their **Non-Performing Asset (NPA)** levels. Rather than relying solely on historical reports and reactive recovery measures, the project aims to shift credit risk management toward a proactive approach by combining **Business Intelligence**, **Exploratory Data Analysis**, and **Machine Learning** to detect early warning signals before defaults occur.

To achieve this objective, the project focuses on analyzing historical loan portfolio performance, integrating macroeconomic indicators, and uncovering hidden relationships that influence credit risk across different lending segments. The analytical insights are further transformed into an interactive decision-support dashboard and a predictive machine learning model capable of forecasting future portfolio deterioration.

The project was designed around the following key objectives:

* Develop a predictive model capable of forecasting future NPA deterioration using historical portfolio performance.
* Understand the major business and economic factors influencing credit risk across different loan segments.
* Perform comprehensive exploratory data analysis to identify trends, anomalies, and portfolio behaviour.
* Design an interactive Power BI dashboard that enables stakeholders to monitor portfolio performance and risk dynamically.
* Generate actionable business recommendations that support proactive credit risk management and strategic decision-making.

Ultimately, the project demonstrates how modern analytics techniques can transform raw financial data into meaningful business intelligence that supports faster, smarter, and evidence-based lending decisions.

---

# 📂 Dataset Overview

A robust predictive model depends heavily on the quality and completeness of its underlying data. To capture both internal portfolio behaviour and external economic influences, this project combines three complementary datasets that together provide a holistic view of loan performance.

### Loan-Level Dataset

The loan-level dataset serves as the foundation of the analysis by capturing detailed information about individual loans across five major lending categories:

* SME Loans
* Home Loans
* Personal Loans
* Agriculture Loans
* Education Loans

The dataset contains important attributes including loan amount, interest rate, tenure, recovery amount, default status, and other transactional information that describes borrower behaviour and portfolio performance.

---

### Macroeconomic Dataset

Since credit risk is strongly influenced by the economic environment, a separate macroeconomic dataset was integrated into the analysis. This dataset includes quarterly indicators such as:

* GDP Growth
* Repo Rate
* Consumer Price Index (CPI)
* Agricultural Production Index
* Unemployment Rate

These variables provide economic context that helps explain fluctuations in borrower repayment capacity beyond portfolio-specific factors.

---

### Master Segment Dataset

The final analytical dataset was created by integrating the loan-level and macroeconomic datasets into a consolidated quarterly segment-level table. This master dataset contains aggregated financial indicators such as Total Advances, Gross NPA, Net NPA, Provision Rate, Recovery Amount, and economic variables for each loan segment.

This integrated dataset served as the primary source for exploratory analysis, dashboard development, feature engineering, and predictive modeling.

---

# 🧹 Data Preparation & Preprocessing

Before beginning the analytical process, extensive data preparation was performed to ensure the quality, consistency, and reliability of the dataset. Since the data originated from multiple sources, it required several preprocessing steps before it became suitable for business analysis and machine learning.

The preprocessing workflow included:

* Standardizing date formats and converting them into chronological time-series data.
* Cleaning percentage values, currency symbols, and formatted numeric fields.
* Converting textual data into numerical representations.
* Handling missing and inconsistent values.
* Sorting observations chronologically for time-dependent analysis.
* Validating data quality across all loan segments.

Python (Pandas and NumPy) was primarily used for data cleaning and transformation, while Power Query in Power BI supported initial data integration and validation.

These preprocessing steps ensured that subsequent analytical findings and machine learning predictions were built on accurate, structured, and reliable data.

---

# 📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis formed one of the most important phases of the project. Before developing the prediction model, it was essential to understand the overall behaviour of the loan portfolio, identify hidden trends, compare segment performance, and discover the business factors contributing to rising Non-Performing Assets.

Using **Microsoft Power BI**, an interactive analytical dashboard was developed to transform raw financial data into meaningful business insights. Rather than focusing only on descriptive statistics, the dashboard provides a multi-dimensional view of portfolio performance, enabling stakeholders to monitor loan health, compare segments, and identify emerging risks through intuitive visualizations.

The analysis was divided into several key areas:

### Portfolio Performance Analysis

This section evaluates the overall financial health of the institution by monitoring Total Advances, Gross NPA, Net NPA, Recovery Amounts, Provision Rates, and portfolio growth across multiple years. The analysis highlights periods of expansion, deterioration, and recovery while providing executives with a high-level understanding of portfolio performance.

---

### Segment-Level Risk Analysis

Each loan category was analyzed individually to understand differences in repayment behaviour and credit quality. Comparative analysis revealed that different loan segments exhibit distinct risk characteristics, emphasizing the importance of segment-specific lending strategies rather than a uniform credit policy.

---

### Time Series Trend Analysis

Historical quarterly data was analyzed to understand how portfolio performance evolved over time. This analysis helped identify recurring deterioration cycles, long-term growth trends, seasonal variations, and the timing of significant portfolio stress.

Understanding these temporal patterns provided valuable context for both predictive modeling and strategic planning.

---

### Macroeconomic Impact Analysis

Credit risk does not depend solely on borrower behaviour. External economic conditions also play a major role in influencing repayment capacity.

This analysis examined how indicators such as GDP Growth, Repo Rate, Inflation (CPI), and Agricultural Production affected portfolio performance across different loan segments.

The findings demonstrated a strong relationship between adverse economic conditions and increasing NPA levels, reinforcing the importance of incorporating macroeconomic variables into predictive risk models.

---

### Loan-Level Behaviour Analysis

Detailed borrower characteristics such as loan tenure, interest rates, loan amount, recovery behaviour, and default status were analyzed to identify common attributes associated with higher default probability.

These insights later became valuable inputs during the feature engineering phase.

---

# 📈 Interactive Power BI Dashboard

To enable intuitive business monitoring, an interactive Power BI dashboard was developed that consolidates all analytical findings into a single decision-support platform.

The dashboard enables users to dynamically explore portfolio performance through filters, drill-down analysis, and interactive visualizations.

Major dashboard components include:

* Executive Portfolio Summary
* Segment-wise Loan Performance
* Gross NPA Trend Analysis
* Recovery Performance Analysis
* Time Series Portfolio Monitoring
* Macroeconomic Impact Dashboard
* Comparative Loan Segment Analysis
* Key Performance Indicator (KPI) Cards

Rather than presenting static reports, the dashboard provides a real-time analytical environment that allows business users to identify emerging risks, compare portfolio behaviour across segments, and make informed lending decisions based on visual insights.

---

# ⚙️ Feature Engineering

After completing exploratory analysis, additional predictive variables were engineered to improve the machine learning model's ability to capture hidden patterns within the data.

Instead of relying solely on raw financial variables, new features were created to represent portfolio momentum, historical trends, and macroeconomic influence.

The engineered features include:

* Historical GNPA Lag Features
* Rolling Average of Total Advances
* Quarter-over-Quarter Portfolio Growth
* Lagged GDP Growth
* Lagged Inflation (CPI)
* Lagged Repo Rate

These features enabled the model to understand not only the current portfolio condition but also how previous financial performance and changing economic environments influence future credit risk.

---

# 🤖 Machine Learning Model

The predictive component of the project was developed using a **Random Forest Classification Model**, selected for its robustness, interpretability, and ability to capture complex nonlinear relationships commonly observed in financial data.

A time-based validation strategy was implemented to simulate real-world forecasting conditions by training the model on historical quarters and evaluating it on future observations. This approach minimizes data leakage and produces a more realistic estimate of predictive performance.

The model learns relationships between historical loan performance, engineered portfolio indicators, and macroeconomic conditions to estimate the probability of future NPA deterioration for each loan segment.

---

# 📊 Model Evaluation & Results

The predictive model demonstrated strong classification performance across multiple evaluation metrics.

| Evaluation Metric | Performance |
| ----------------- | ----------: |
| Precision         |    **100%** |
| Recall            |    **100%** |
| F1-Score          |     **93%** |
| AUC-ROC           |   **91.3%** |

Feature importance analysis further revealed that historical GNPA trends, portfolio growth patterns, and macroeconomic indicators were the strongest predictors of future portfolio deterioration.

These results indicate that combining financial performance data with broader economic context significantly improves the model's predictive capability.

---

# 💡 Key Business Insights

The analytical findings generated several important business insights that extend beyond predictive accuracy.

The project identified that **SME and Personal Loan portfolios exhibited the highest volatility**, making them more susceptible to future deterioration under adverse economic conditions. In contrast, **Home Loans demonstrated greater stability**, reflecting the lower risk associated with secured lending.

Time-series analysis revealed that rapid portfolio expansion often preceded increases in GNPA, suggesting that aggressive credit growth should be accompanied by stronger monitoring and underwriting practices. Additionally, macroeconomic indicators such as GDP growth, inflation, and interest rate movements showed a measurable influence on repayment behaviour, highlighting the importance of integrating external economic conditions into credit risk assessment.

These findings demonstrate that effective risk management requires a balanced understanding of both internal portfolio performance and the broader economic environment.

---

# 📌 Business Recommendations

Based on the analytical findings and machine learning predictions, several strategic recommendations were proposed to improve portfolio stability and strengthen credit risk management.

### Early Warning System (EWS)

Implement an automated Early Warning System that continuously monitors high-risk loan segments and generates alerts when the probability of deterioration exceeds predefined thresholds. Early intervention enables institutions to take corrective action before defaults occur.

### Risk-Based Portfolio Monitoring

Allocate greater monitoring resources to loan segments exhibiting higher predicted risk while maintaining routine oversight for lower-risk portfolios. This targeted approach improves operational efficiency and ensures that risk management efforts are focused where they create the greatest value.

### Loan Restructuring Strategies

Provide flexible repayment options, revised repayment schedules, or temporary interest adjustments for borrowers demonstrating early signs of financial stress. Proactive restructuring can significantly reduce future defaults and improve portfolio quality.

### Dynamic Credit Policies

Use predictive insights to refine lending policies by adjusting approval criteria, pricing strategies, and exposure limits according to segment-level risk. Data-driven lending decisions help balance portfolio growth with long-term financial stability.

### Continuous Economic Monitoring

Incorporate macroeconomic indicators such as GDP growth, inflation, and interest rates into ongoing portfolio monitoring. Tracking changes in the economic environment enables institutions to anticipate shifts in repayment behaviour and respond proactively to emerging risks.

---
