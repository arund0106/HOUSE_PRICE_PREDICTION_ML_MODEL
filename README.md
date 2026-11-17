# 🏠 House Price Prediction using Linear Regression

A beginner-friendly machine learning project that predicts house prices from features such as area, bedrooms, bathrooms and amenities, using **Linear Regression** in Python.

---

## 📌 Overview

Buying or selling a house starts with one question: *what is it worth?* This project builds a regression model that estimates house price from the property's characteristics, and looks at which features matter most.

**Workflow:** Load data → Explore & visualize → Preprocess → Train model → Evaluate

---

## 📂 Dataset

| Item | Details |
|---|---|
| File | `Housing.csv` |
| Records | 545 houses |
| Features | 12 input features |
| Target | `price` |
| Missing values | None |
| Duplicate rows | None |

| Type | Columns |
|---|---|
| **Numeric** | `area`, `bedrooms`, `bathrooms`, `stories`, `parking` |
| **Yes / No** | `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea` |
| **Categorical** | `furnishingstatus` (furnished, semi-furnished, unfurnished) |

---

## 📚 Libraries

| Library | Purpose |
|---|---|
| **Pandas** | Data loading and manipulation |
| **Scikit-learn** | Scaling, Linear Regression, evaluation (R²) |
| **Seaborn** | Statistical visualizations |
| **Matplotlib** | Plotting |

---

## 🔄 Steps

1. **Import libraries and dataset**
2. **Data understanding**: checked shape (545 × 13) and data types
3. **Encoding**
   - Converted the six yes/no columns to 1/0
   - Converted `furnishingstatus` to numbers (furnished = 0, unfurnished = 1, semi-furnished = 2)
4. **Scaling:** standardized `price` and `area` with `StandardScaler`
5. **Exploratory checks**
   - Linearity: scatter plot with regression line (`area` vs `price`)
   - Normality: distribution plots of `area` and `price`
   - Correlation: heatmap of all features
6. **Data preparation:** separated features (`X`) and target (`y`)
7. **Model building and training:** fitted a `LinearRegression` model
8. **Testing and evaluation:** generated predictions, calculated residuals and the **R² score**, and plotted actual vs. predicted prices

---

## 📈 Results

| Metric | Value |
|---|---|
| **R² Score** | **0.67** (the model explains about 67% of the variation in house prices) |

**Features most correlated with price:** `area` (0.54), `bathrooms` (0.52), `airconditioning` (0.45), `stories` (0.42)

**Key takeaways**
- Larger houses and houses with more bathrooms tend to cost more
- Air conditioning, hot water heating and a preferred area are linked to higher prices
- Number of bedrooms and furnishing status have only a small effect once other features are included

### 🔭 Limitations and Next Steps
This is my first ML project, so there is room to improve:
- [ ] Split the data into **train and test sets** (the current score is calculated on the same data the model was trained on)
- [ ] Use **one-hot encoding** for `furnishingstatus`, since it has no natural order
- [ ] Add more metrics such as **MAE** and **RMSE**
- [ ] Try other models (Ridge, Random Forest) and compare them

---

## ▶️ How to Run

**1. Clone the repository**
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

**2. Install the required libraries**
```bash
pip install pandas scikit-learn seaborn matplotlib jupyter
```

**3. Launch the notebook**
```bash
jupyter notebook Linear_Reg_ML.ipynb
```
Run all cells from top to bottom. Keep `Housing.csv` in the same folder as the notebook.

---

## 📁 Project Structure

```
├── Housing.csv            # Dataset
├── Linear_Reg_ML.ipynb    # Notebook (analysis and model)
└── README.md
```

---

## 👤 Author

**Arun D**
🔗 [*Add your LinkedIn / Portfolio link here*](https://linkedin.com/in/arun-durai-d162005/)
