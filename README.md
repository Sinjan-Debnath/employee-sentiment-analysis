# 🧠 Employee Sentiment Analysis

This project analyzes internal employee communications to uncover sentiment trends, identify key influencers, and detect potential employee flight risks using NLP and predictive modeling.

---

## 📋 Overview

This analysis was conducted on **2,191 employee messages** (from May 2010 to January 2011) to evaluate overall sentiment and uncover actionable insights for HR and organizational health monitoring.

A **RoBERTa transformer model** was used for sentiment classification, while a **Linear Regression model** was developed to predict monthly sentiment trends based on communication patterns.

---

## 🚀 Features

- **Sentiment Classification:** Uses `cardiffnlp/twitter-roberta-base-sentiment-latest` to categorize each message as **Positive**, **Neutral**, or **Negative**.  
- **Employee Scoring:** Assigns +1 to positive and -1 to negative messages to calculate monthly sentiment scores.  
- **Flight Risk Detection:** Flags employees with 4+ negative messages in any rolling 30-day window.  
- **Predictive Modeling:** Builds a regression model to forecast monthly sentiment changes based on message count and length.  
- **Visualization:** Time-series and distribution plots for sentiment analysis trends.

---

## 🧰 Tech Stack

| Component | Tool/Library |
|------------|---------------|
| Programming Language | Python 3.x |
| NLP Model | RoBERTa (`cardiffnlp/twitter-roberta-base-sentiment-latest`) |
| Data Analysis | pandas, numpy |
| Visualization | matplotlib, seaborn |
| Machine Learning | scikit-learn (LinearRegression) |
| Environment | Jupyter Notebook |

---

## 📂 Repository Structure

- **employee-sentiment-analysis/**
  - **data/** — Dataset (internal employee messages)
  - **visualization/** — Plots and charts generated during analysis
  - **employee_sentiment_analysis.ipynb** — Main Jupyter notebook
  - **Employee Sentiment Analysis Report.pdf** — Final analytical report
  - **README.md** — Project documentation


---

## 📈 Key Insights

- **Overall Sentiment**
  - Positive: **19.4%**
  - Negative: **5.2%**
  - Neutral: **75.5%**

- **Top Positive Employees**
  1. johnny.palmer@enron.com (2.04)  
  2. bobette.riner@ipgdirect.com (1.75)  
  3. sally.beck@enron.com (1.75)

- **Flagged Flight Risk**
  - john.arnold@enron.com (frequent negative sentiment spikes)

- **Model Performance**
  - Linear Regression R² = **0.1206**
  - Most influential predictor: `monthly_msg_count`

---

## 💡 Recommendations

1. **Engage with Flagged Employee:**  
   Confidentially address issues with the flagged individual to identify potential concerns.

2. **Recognize Positive Influencers:**  
   Leverage top positive contributors as cultural ambassadors to improve overall morale.

3. **Continuous Monitoring:**  
   Re-run sentiment analysis quarterly to detect early warning signs and measure improvement.

---

## 📘 Methodology

1. **Data Cleaning**  
   - Removed missing values  
   - Converted date strings to datetime objects  
   - Standardized employee identifiers  

2. **Sentiment Classification**  
   - Applied RoBERTa model on each message  
   - Stored results as sentiment labels and confidence scores  

3. **Scoring & Aggregation**  
   - Calculated per-employee monthly sentiment scores  
   - Ranked top positive and negative contributors  

4. **Predictive Modeling**  
   - Trained Linear Regression model using:
     - Monthly message count  
     - Average message length  
   - Evaluated performance with R² and visualized feature importance  

---

## 📊 Results Visualization

Visual outputs include:

- Sentiment distribution plots  
- Monthly sentiment trend line  
- Employee sentiment rankings  
- Feature importance chart for the predictive model  

---

## 🧩 Limitations

- Small dataset (≈2,000 messages) limits statistical generalization  
- Only 12% variance explained by regression model  
- Does not yet include linguistic or contextual feature engineering  

---

## 🧭 Future Work

- Integrate **BERT-based multilingual models** for broader datasets  
- Add **temporal sentiment lag features** for improved forecasting  
- Build a **dashboard** (Streamlit / React + Flask) for real-time HR monitoring  

---

## 📄 License

This project is released under the [MIT License](LICENSE).




