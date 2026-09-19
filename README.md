# 📊 Customer Churn Analysis

## 📌 Project Overview

This project analyzes customer churn using Python and exploratory data analysis (EDA).

The objective is to understand customer churn patterns and identify how factors such as contract type, customer tenure, city, monthly charges, support calls, payment method, satisfaction score, age group, and plan type are associated with customer churn.

---

## 🎯 Business Questions

1. What percentage of customers have churned?
2. Which contract type has the highest churn?
3. Does customer tenure affect churn?
4. Which cities have the highest churn?
5. Does monthly charge affect churn?
6. Do customers with more support calls churn more?
7. Which payment method has the highest churn?
8. Does customer satisfaction relate to churn?
9. How does churn vary by age group?
10. Which plan type generates the most revenue while also having a high churn rate?

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📂 Dataset

The dataset contains **5,000 customer records** and includes customer, service, financial, and satisfaction information.

### Main Columns

- Customer_ID
- Gender
- Age
- City
- Tenure_Months
- Contract_Type
- Plan_Type
- Internet_Service
- Payment_Method
- Monthly_Charges
- Total_Charges
- Data_Usage_GB
- Support_Calls
- Late_Payments
- Satisfaction_Score
- Discount_Percent
- Churn

---

## 🧹 Data Cleaning

The following data-cleaning steps were performed:

- Loaded the customer churn CSV dataset
- Inspected the dataset using `head()`, `shape()`, `info()`, and `describe()`
- Converted blank values into missing values
- Checked missing values
- Filled missing numerical values using the median
- Filled missing categorical values using the mode
- Checked for duplicate records
- Created additional analytical groups for tenure, monthly charges, and age

---

# 📊 Exploratory Data Analysis

## 1. Overall Customer Churn

The dataset contains:

- **3,910 customers who did not churn**
- **1,090 customers who churned**
- **Overall churn rate: 21.8%**

This means approximately 21.8% of customers in the dataset have a churn status of "Yes".

---

## 2. Churn by Contract Type

| Contract Type | Churn Rate |
|---|---:|
| Monthly | 24.43% |
| Quarterly | 20.45% |
| Yearly | 16.10% |

The observed churn rate is highest among customers with monthly contracts.

---

## 3. Churn by Customer Tenure

| Tenure Group | Churn Rate |
|---|---:|
| 0–12 months | 31.49% |
| 13–24 months | 24.35% |
| 25–36 months | 16.90% |
| 37–48 months | 12.93% |
| 49–60 months | 8.51% |

The analysis shows a higher observed churn rate among customers with shorter tenure.

---

## 4. Churn by City

| City | Churn Rate |
|---|---:|
| Chennai | 24.90% |
| Hyderabad | 23.38% |
| Bengaluru | 22.75% |
| Kolkata | 21.61% |
| Delhi | 21.48% |
| Pune | 20.97% |
| Mumbai | 20.91% |
| Jaipur | 20.06% |
| Ahmedabad | 19.95% |
| Kochi | 18.75% |

Chennai has the highest observed churn rate among the cities in the dataset.

---

## 5. Churn by Monthly Charges

Customers were divided into four monthly-charge groups using quartiles.

| Monthly Charge Group | Churn Rate |
|---|---:|
| Low | 17.36% |
| Medium-Low | 20.62% |
| Medium-High | 22.33% |
| High | 26.96% |

The observed churn rate increases across the monthly-charge groups, with the highest-charge group having a churn rate of 26.96%.

---

## 6. Churn by Support Calls

| Support Calls | Churn Rate |
|---:|---:|
| 0 | 12.50% |
| 1 | 15.70% |
| 2 | 19.71% |
| 3 | 24.42% |
| 4 | 33.97% |
| 5 | 37.30% |
| 6 | 41.67% |
| 7 | 57.69% |
| 8 | 66.67% |
| 9 | 100.00% |
| 10 | 100.00% |

The analysis shows an increasing observed churn rate as the number of support calls increases.

The 9 and 10 support-call groups should be interpreted carefully because their customer counts may be smaller.

---

## 7. Churn by Payment Method

| Payment Method | Churn Rate |
|---|---:|
| Cash | 26.10% |
| Credit Card | 23.77% |
| UPI | 20.96% |
| Bank Transfer | 20.55% |
| Debit Card | 19.75% |

Cash has the highest observed churn rate among the payment methods in the dataset.

---

## 8. Churn by Satisfaction Score

| Satisfaction Score | Churn Rate |
|---:|---:|
| 1 | 0.00% |
| 2 | 100.00% |
| 3 | 73.33% |
| 4 | 50.24% |
| 5 | 32.65% |
| 6 | 24.21% |
| 7 | 18.90% |
| 8 | 13.33% |
| 9 | 12.29% |
| 10 | 9.64% |

The dataset shows higher observed churn rates at lower satisfaction scores.

Some individual satisfaction-score groups may contain relatively few customers, so the percentages should be interpreted together with sample size.

---

## 9. Churn by Age Group

| Age Group | Churn Rate |
|---|---:|
| 18–25 | 22.79% |
| 26–35 | 23.67% |
| 36–45 | 21.10% |
| 46–55 | 21.69% |
| 56–65 | 21.14% |
| 66+ | 19.67% |

The 26–35 age group has the highest observed churn rate among the age groups.

---

# 💰 10. Revenue and Churn by Plan Type

The dataset does not contain a separate `Customer_Segment` column.

Therefore, **Plan_Type** was used to analyze revenue and churn across customer plans.

| Plan Type | Revenue | Churn Rate |
|---|---:|---:|
| Standard | ₹55.81M | 21.67% |
| Basic | ₹32.87M | 18.81% |
| Premium | ₹32.49M | 27.65% |

### Observation

The **Standard plan generated the highest total revenue**, approximately **₹55.81 million**.

The **Premium plan had the highest observed churn rate**, approximately **27.65%**.

This provides a useful comparison between revenue contribution and observed customer churn across plan types.

---

# 📈 Visualizations

The analysis includes visualizations for:

- Customer Churn Distribution
- Churn Rate by Contract Type
- Churn Rate by Customer Tenure
- Churn Rate by City
- Churn Rate by Monthly Charges
- Churn Rate by Support Calls
- Churn Rate by Payment Method
- Churn Rate by Satisfaction Score
- Churn Rate by Age Group
- Revenue by Plan Type
- Churn Rate by Plan Type

---

# 💡 Key Business Observations

- Overall customer churn is **21.8%**.
- Monthly contracts have the highest observed churn rate among contract types.
- Customers with shorter tenure show higher observed churn rates.
- The highest monthly-charge group has a higher observed churn rate than the lowest group.
- Churn rate increases as support calls increase in this dataset.
- Cash payment users have the highest observed churn rate among payment methods.
- Lower satisfaction scores are associated with higher observed churn rates.
- The 26–35 age group has the highest observed churn rate among the age groups.
- The Standard plan generates the highest total revenue.
- The Premium plan has the highest observed churn rate among the three plans.

> **Note:** These are descriptive findings from this dataset. They show relationships observed in the data and should not automatically be interpreted as proof that one factor directly causes customer churn.

---

# 📁 Project Structure

```text
customer-churn-analysis/
│
├── customer churn analysis.ipynb
├── customer_churn.csv
└── README.md
