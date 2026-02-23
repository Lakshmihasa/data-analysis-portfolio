# ⚽ Sports Analytics: FIFA Player Performance & Rating Prediction

## 📌 Project Overview
This project analyzes professional football player data from the FIFA dataset to understand performance patterns across positions and to predict a player’s overall rating using machine learning techniques.

The goal is to demonstrate end-to-end data analysis skills including data cleaning, exploratory data analysis (EDA), feature engineering, regression modeling, and business insight generation.

---

## 📂 Dataset
- Source: FIFA 21 Players Dataset (Kaggle)
- Size: 20,000+ players
- Data includes:
  - Player demographics (age, nationality)
  - Position information
  - Skill attributes (pace, shooting, passing, etc.)
  - Overall rating and potential

Goalkeepers were excluded from modeling due to fundamentally different skill attributes.

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 🔍 Exploratory Data Analysis (EDA)
Key EDA steps included:
- Distribution analysis of overall ratings
- Age vs performance analysis
- Position-wise comparison of player ratings
- Skill distribution analysis using heatmaps

### Key Observations:
- Attacking players tend to have higher pace and shooting
- Defensive roles rely more on physic and defending skills
- Certain positions peak earlier in age compared to others

---

## 🤖 Machine Learning Model
### Problem Type:
Regression — Predicting player overall rating

### Features Used:
- Age
- Pace
- Shooting
- Passing
- Dribbling
- Defending
- Physic

### Models Implemented:
1. Linear Regression (baseline model)
2. Random Forest Regressor (improved performance)

### Evaluation Metrics:
- RMSE (Root Mean Squared Error)
- R² Score

The Random Forest model achieved better predictive performance, capturing non-linear relationships between skills and overall rating.

---

## 📊 Model Evaluation & Error Analysis
- Actual vs Predicted scatter plots were used to visualize model performance
- Error distribution analysis showed predictions centered around zero
- Higher-rated elite players showed larger prediction variance, indicating influence of unobserved factors

---

## ⚽ Sports & Business Insights
- Skill attributes are strong indicators of player overall rating
- Players with strong skills but lower ratings may represent undervalued talent
- Overall rating alone should not be used for recruitment decisions
- Position-specific analysis improves scouting and squad planning

---

## 📈 Recommendations
- Use skill-based analytics for talent identification
- Build position-specific models for better prediction accuracy
- Avoid one-size-fits-all player evaluation metrics
- Combine data-driven insights with tactical and contextual knowledge

---

## 📁 Project Structure
project3_sports_analytics/
├── data/
│ ├── players_21.csv
│ └── clean_players_21.csv
├── notebooks/
│ └── 01_data_loading_and_eda.ipynb
├── visuals/
└── README.md

---

## ✅ Conclusion
This project demonstrates a complete sports analytics workflow — from raw data to actionable insights — and highlights how data science can support decision-making in professional sports environments.