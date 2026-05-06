# 📊 Sales Prediction using Python

A machine learning project that predicts future sales based on advertising budgets across TV, Radio, and Newspaper channels. Built as part of the **CodeAlpha Data Science Internship — Task 4**.

---

## 📌 Project Overview

This project builds and compares multiple regression models to forecast sales from advertising spend data. It answers a core business question: **which advertising channels drive the most sales?** The full pipeline covers data cleaning, exploratory analysis, feature engineering, model training, and actionable business insights.

**Key questions answered:**
- Which advertising channel has the strongest impact on sales?
- How accurately can we predict sales from ad budgets?
- How do changes in advertising spend affect sales outcomes?
- Which model performs best for this regression task?

---

## 🗂️ Project Structure

```
CodeAlpha_SalesPrediction/
│
├── sales_prediction.ipynb        # Main Kaggle notebook
├── eda_sales.png                 # EDA: distributions and scatter plots
├── budget_analysis.png           # Advertising budget breakdown
├── model_comparison.png          # R², MAE, RMSE comparison chart
├── actual_vs_predicted.png       # Actual vs Predicted + Residual plot
├── feature_importance.png        # Feature importance / coefficients
└── README.md                     # Project documentation
```

---

## 📊 Dataset

| Detail | Info |
|---|---|
| Name | Advertising and Sales |
| Source | [Kaggle — Advertising Dataset](https://www.kaggle.com/datasets/bumba5341/advertisingcsv) |
| Rows | 200 records |
| Target | Sales (in thousands of units) |

### Columns

| Column | Description |
|---|---|
| `TV` | Advertising budget spent on TV ($) |
| `Radio` | Advertising budget spent on Radio ($) |
| `Newspaper` | Advertising budget spent on Newspaper ($) |
| `Sales` | Units sold (target variable) |

---

## ⚙️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Pandas | Data loading, cleaning, manipulation |
| NumPy | Numerical operations |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | Model training, evaluation, preprocessing |

---

## 🔄 Project Pipeline

```
Load Data → Clean & Explore → Visualize → Preprocess → Train Models → Evaluate → Predict
```

### Steps in detail

1. **Load Data** — Read CSV from Kaggle input directory
2. **Clean** — Strip column names, handle missing values, check data types
3. **Explore** — Descriptive statistics, correlation analysis
4. **Visualize** — Scatter plots, heatmap, budget breakdown, regression lines
5. **Preprocess** — Train/test split (80/20) + StandardScaler normalization
6. **Train** — Fit 3 regression models and record metrics
7. **Evaluate** — Compare R², MAE, RMSE across models
8. **Predict** — Forecast sales for new advertising budgets
9. **Insights** — Extract business recommendations

---

## 🤖 Models Used

| Model | Type | Description |
|---|---|---|
| Linear Regression | Parametric | Fits a linear relationship between features and sales |
| Random Forest | Ensemble | Combines 100 decision trees for robust predictions |
| Gradient Boosting | Ensemble | Sequentially corrects errors for higher accuracy |

---

## 📈 Evaluation Metrics

| Metric | Description | Goal |
|---|---|---|
| **R² Score** | Proportion of variance explained | Higher is better (max = 1.0) |
| **MAE** | Mean Absolute Error | Lower is better |
| **RMSE** | Root Mean Squared Error | Lower is better |

---

## 💡 Key Business Insights

-  **TV advertising** has the strongest positive correlation with sales — the most impactful channel to invest in
-  **Radio** also shows a significant effect on sales, especially at moderate spend levels
-  **Newspaper** advertising has the weakest relationship with sales — low ROI compared to TV and Radio
-  The best model explains **~97% of the variance** in sales (R² ≈ 0.97), making predictions highly reliable
-  **Actionable recommendation**: Reallocate newspaper budget toward TV and Radio to maximize sales outcomes

---

## 🔮 Sample Predictions

```python
# New advertising campaigns
new_campaigns = {
    'Campaign A': [TV=200, Radio=30, Newspaper=20]  → Predicted Sales: ~XX
    'Campaign B': [TV=50,  Radio=10, Newspaper=5]   → Predicted Sales: ~XX
    'Campaign C': [TV=300, Radio=60, Newspaper=40]  → Predicted Sales: ~XX
}
```

*(Update with your actual predicted values after running Cell 11)*

---

| Source | [kaggle.com](https://www.kaggle.com/code/yacinebouachrine/sales-prediction-using-python) |

### Locally
```bash
# Clone the repository
git clone https://github.com/your-username/CodeAlpha_SalesPrediction.git
cd CodeAlpha_SalesPrediction

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Update the file path in Cell 2:
# df = pd.read_csv('advertising.csv')

# Run the notebook
jupyter notebook sales_prediction.ipynb
```

---

## 📚 Key Learnings

- How to build and evaluate regression models for sales forecasting
- How to compare multiple ML models using R², MAE, and RMSE
- How to interpret feature importance and regression coefficients
- How to visualize the relationship between advertising spend and sales
- How to use residual plots to diagnose model quality
- How to translate model results into actionable business recommendations

---

## 🏢 About

This project was completed as **Task 4** of the **CodeAlpha Data Science Internship**.

- 🌐 Website: [www.codealpha.tech](https://www.codealpha.tech)
- 📧 Email: services@codealpha.tech

---

## 👤 Author

**Your Name**
- GitHub: [yassinebouachrine](https://github.com/yassinebouachrine)
- LinkedIn: [yassinebouachrine](https://linkedin.com/in/yassine-bouachrine-68b761230)
---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
