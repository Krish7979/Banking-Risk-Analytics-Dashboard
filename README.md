
# 🏦 Banking Risk Analytics Dashboard (Power BI)

## 📌 Project Overview
This project is based on **Banking Risk Analytics** using **Power BI**. The objective is to analyze banking data and understand customer behavior related to **loans, deposits, income bands, and banking relationships** to minimize financial risk while lending.

---

## 🎯 Problem Statement
Develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimize the risk of losing money while lending to customers.

---

## 💡 Solution
Using interactive Power BI dashboards, banks can:
- Analyze applicant profiles
- Identify customers likely to repay loans
- Make informed loan approval decisions
- Monitor deposits, loans, and client engagement

---

## 📊 Dashboards Included

### 🏠 Home Dashboard
- Overall banking overview
- Total clients, loans, and deposits
- Savings & checking accounts summary

### 💰 Loan Analysis Dashboard
- Total Loan, Bank Loan & Business Lending
- Loan distribution by:
  - Banking Relationship
  - Occupation
  - Income Band
  - Nationality
- Credit Card Balance

### 💳 Deposit Analysis Dashboard
- Total Deposit breakdown
- Bank Deposit, Savings & Checking Accounts
- Deposits by:
  - Income Band
  - Occupation
  - Nationality
  - Banking Relationship

### 📈 Summary Dashboard
- High-level KPIs
- Combined financial overview

---

## 🗂️ Dataset Description
The dataset contains banking and client-level data across multiple interlinked tables using **primary and foreign keys**.

### Tables Used:
- Clients – Banking
- Banking Relationship
- Gender
- Investment Advisor
- Period

---

## 🧹 Data Cleaning & Feature Engineering
- Created **Engagement Timeframe**
- Calculated **Engagement Days**
- Created **Income Band**:
  - Low: < 100000
  - Medium: < 300000
  - High: > 300000
- Created **Processing Fees** based on Fee Structure

---

## 🧮 DAX Measures Used

```DAX
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID])

Total Loan = [Bank Loan] + [Business Lending] + [Credit Cards Balance]

Total Deposit =
[Bank Deposit] + [Savings Account] +
[Foreign Currency Account] + [Checking Accounts]

Total Fees =
SUMX('Clients - Banking',
     [Total Loan] * 'Clients - Banking'[Processing Fees])
```

### DAX Functions
- SUM
- SUMX
- DISTINCTCOUNT
- SWITCH
- DATEDIFF

---

## 📌 Key KPIs
- Total Clients
- Total Loan
- Bank Loan
- Business Lending
- Total Deposit
- Savings Account Amount
- Checking Account Amount
- Credit Card Balance
- Engagement Length
- Total Fees

---

## 📈 Insights
- Medium income group contributes the highest share of loans and deposits
- Private banks have more active clients
- Nationality and occupation significantly impact loan distribution
- Banking relationship helps in risk segmentation

---

## ✅ Conclusion
This Power BI dashboard provides actionable insights that help banks:
- Reduce lending risk
- Improve loan approval strategies
- Understand customer financial behavior
- Make data-driven decisions

---

## 🔮 Future Scope
- Loan default prediction using ML
- Advanced customer segmentation
- Trend analysis across multiple years
- Real-time banking analytics

---

## 🛠 Tools & Technologies
- Power BI
- DAX
- Excel / CSV Dataset

---

## 👤 Author
**Krish Modi**  
B.Tech IT Student  
Data Analytics | Power BI | Python | C
