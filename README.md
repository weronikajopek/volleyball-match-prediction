# Volleyball Match Prediction & Strategy Visualisation 🏐

### 🎓 Engineering Thesis
**"Machine Learning-driven volleyball match prediction and play strategy visualisation"** This project uses 15 years of Polish **PlusLiga (2008–2023)** data to predict the exact results of professional matches.

---

## 🎯 The Goal
The primary goal was the **multiclass classification problem**. Instead of a simple win/loss binary, the model predicts the **exact match outcome** from the home team's perspective across 6 distinct classes:
* **3:0, 3:1, 3:2** (Home Team Victories)
* **2:3, 1:3, 0:3** (Home Team Defeats)

---

## 🛠️ How it Works
The project follows a 5-step pipeline:

1. **Preprocessing:** Reorganized match data to track team progress over time. Calculated **rolling averages** to capture each team's current "form."
2. **EDA (Data Exploration):** Analyzed league trends and used a **correlation matrix** to see which stats (like blocks or serve aces) affect the final score the most.
3. **Feature Engineering:** Created "Difference Features"—calculating the performance gap between the two competing teams to help the model decide the winner.
4. **Modeling:** Trained and tested four different models:
   * **Random Forest (RF)**
   * **Logistic Regression (LR)**
   * **XGBoost**
   * **SVM**
5. **Visualisations:** Created charts to evaluate **team form** and help visualize play strategies throughout the season.

---

## 📂 Repository Structure
```text
├── data/
│   ├── Mens-Volleyball-PlusLiga-2008-2023.csv   # Raw Dataset
│   └── final_df.csv                             # Processed Feature Set
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── eda.ipynb
│   ├── feature-engineering.ipynb
│   ├── visualizations.ipynb
│   └── models.ipynb
├── plots/                                       # Generated Charts & Result Plots
├── requirements.txt                             # Python Dependencies
└── README.md
