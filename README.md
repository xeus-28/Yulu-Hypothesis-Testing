🚲 Yulu – Hypothesis Testing Analysis
📌 Project Overview

This project performs statistical hypothesis testing on a bicycle rental dataset to understand how external factors such as working days, holidays, weather conditions, and seasons influence rental demand.
The analysis follows a structured statistical workflow, including assumption checks, appropriate test selection, and business-oriented conclusions.

📊 Dataset Description

The dataset contains 10,886 observations with the following features:

Column	Description
datetime	Date and time of rental
season	Season category (1–4)
holiday	Whether the day is a holiday
workingday	Whether the day is a working day
weather	Weather condition category
temp	Temperature
atemp	Feels-like temperature
humidity	Humidity level
windspeed	Wind speed
casual	Casual users
registered	Registered users
count	Total rental demand
🔬 Hypothesis Testing Methodology

Each hypothesis test follows this structured approach:

Formulate Null (H₀) and Alternative (H₁) hypotheses

Select an appropriate statistical test

Check test assumptions

Set significance level (α = 0.05)

Compute test statistic and p-value

Make a decision (Reject / Fail to Reject H₀)

Draw business inferences and recommendations

🧪 Tests Performed
1️⃣ Working Day vs Non-Working Day

Test Used: 2-Sample Independent T-Test

H₀: Mean rental demand is the same on working and non-working days

Result: Fail to Reject H₀

Insight: Working day status alone does not significantly affect demand

2️⃣ Holiday vs Non-Holiday

Test Used: 2-Sample Independent T-Test

H₀: Mean rental demand is the same on holidays and non-holidays

Insight: Evaluated demand stability across calendar events

3️⃣ Weather Conditions vs Rental Demand

Test Used: One-Way ANOVA

H₀: Mean rental demand is the same across all weather conditions

Levene’s Test: Variance inequality detected

Result: Reject H₀

Insight: Weather conditions significantly influence rental demand

4️⃣ Seasonal Impact on Rental Demand

Test Used: One-Way ANOVA

H₀: Mean rental demand is the same across all seasons

Result: Reject H₀

Insight: Strong seasonal variation exists in rental demand

5️⃣ Weather vs Season Relationship

Test Used: Chi-Square Test of Independence

H₀: Weather conditions and seasons are independent

Result: Reject H₀

Insight: Weather patterns vary significantly across seasons

📈 Assumption Checks

Normality

Histogram, Q-Q plots, Skewness & Kurtosis

Shapiro-Wilk Test (sample-based due to large dataset)

Equality of Variance

Levene’s Test

Analysis continued even when assumptions failed, as ANOVA is robust for large samples, supported by visual inspection.

💡 Key Insights & Recommendations

Weather and Seasonality are strong drivers of bicycle rental demand

Working day status alone does not significantly impact demand

Demand forecasting models should incorporate:

Weather conditions

Seasonal patterns

Operational strategies such as staffing, inventory, and pricing should be weather- and season-aware

Promotional strategies can be designed for low-demand seasons or adverse weather conditions

🛠 Tools & Libraries Used

Python

pandas

NumPy

SciPy

Matplotlib

Seaborn

Jupyter Notebook

✅ Conclusion

This project demonstrates how statistical hypothesis testing can be used to validate assumptions about customer behavior and external factors affecting demand.
The insights gained can be directly applied to operational planning, demand forecasting, and strategic decision-making in bike rental systems.

📌 Future Work

Post-hoc analysis (Tukey’s HSD) for ANOVA results

Regression modeling with season & weather features

Time-series forecasting for rental demand