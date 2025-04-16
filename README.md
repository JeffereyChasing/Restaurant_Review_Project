# 🧠 Foundations of Data Science Project: UberEats Restaurant Analysis

This project explores data from UberEats USA restaurant listings and menus to investigate how cuisine type and price range relate to restaurant scores. By performing descriptive and probabilistic analysis on publicly available datasets, we aim to understand if restaurants serving American cuisine are rated differently than others and whether price range impacts these ratings.

---

## 📁 Datasets

The analysis is based on two related datasets sourced from [Kaggle](https://kaggle.com/datasets/ahmedshahriarsakib/uber-eats-usa-restaurants-menus/data):

### `restaurants.csv`

Contains metadata about UberEats restaurants including:

- `id`: Restaurant ID
- `position`: Search result position
- `name`: Restaurant name
- `score`: User rating score on UberEats
- `ratings`: Number of ratings
- `category`: Restaurant cuisine category
- `price_range`: Pricing tier
- `full_address`, `zip_code`, `lat`, `long`: Location details
- `locality`: Added column indicating if the restaurant serves American cuisine
- `menu_diversity`: Added feature based on variety in the restaurant's menu

### `restaurant-menus.csv`

Details each restaurant's menu offerings:

- `restaurant_id`: Foreign key linking to restaurants
- `category`: Menu category (e.g. main dish, drinks)
- `name`: Item name
- `description`: Item description
- `price`: Item price

---

## 🎯 Objectives

The primary goals of the project are:

- To compare restaurant score distributions between American and non-American cuisines.
- To examine the relationship between restaurant price range and user scores.
- To develop and evaluate a probabilistic model to assess score distributions conditioned on price range and cuisine type.

---

## 🧪 Methodology

The notebook follows these steps:

1. **Data Preprocessing**:
   - Cleaned and merged the two datasets.
   - Derived new features such as `locality` and `menu_diversity`.

2. **Exploratory Data Analysis**:
   - Visualized distributions of scores across different categories.
   - Grouped restaurants by cuisine type and price range to analyze average scores.

3. **Probabilistic Modeling**:
   - Applied Bayesian techniques to estimate the posterior distribution of restaurant scores.
   - Compared posterior predictions across different categories to quantify differences in restaurant performance.

4. **Posterior Predictive Checks**:
   - Simulated samples from the posterior distributions to visualize uncertainty and draw insights.

---

## 📊 Key Insights

- Restaurants that serve non-American cuisine tend to have slightly higher scores on average.
- However, among the highest price-tier restaurants, those offering American cuisine show a higher mean score distribution.
- Bayesian modeling offers a powerful way to incorporate uncertainty and compare overlapping score distributions.

---

## 📦 Tools & Technologies

- **Python 3.x**
- **Pandas** for data wrangling
- **Matplotlib & Seaborn** for visualization
- **PyMC3 / Arviz** for Bayesian modeling and posterior analysis
- **Jupyter Notebook** as the analysis environment

---

## 📌 How to Use

1. Clone the repository or download the notebook.
2. Install required Python packages:
   ```bash
   pip install pandas matplotlib seaborn pymc3 arviz
   ```
3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook FoundationOfDS_project.ipynb
   ```

---

## 📄 Conclusion

This project demonstrates how probabilistic modeling can provide deeper insights into patterns in restaurant ratings data. With thoughtful preprocessing and visualization, we can uncover trends that may guide user expectations or business strategies in food delivery platforms.

---
