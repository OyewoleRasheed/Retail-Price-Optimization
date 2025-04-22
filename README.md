# 🛍️ Retail Price Optimization using Machine Learning

This project demonstrates how to use machine learning to optimize retail pricing strategies in order to maximize revenue. By analyzing features such as quantity sold, product price, competitor pricing, and customer perception scores, the model predicts the **total price** or revenue potential of a product.

---

## 📌 Project Objective

Retailers often struggle to balance pricing to stay competitive, boost sales, and maximize profit.  
This project aims to:

- Predict the **total price** or revenue from product sales
- Use data-driven insights to inform pricing strategies
- Understand the effect of competitors and product quality on revenue

---

## 🔍 Features Used

The model was trained using the following features:

| Feature | Description |
|--------|-------------|
| `qty` | Number of items sold |
| `unit_price` | Price of a single item |
| `comp_1` | Competitor’s price or market influence |
| `product_score` | A rating or quality score of the product |
| `comp_price_diff` | Difference between our price and competitor’s |

The target variable is:

- `total_price`: The total revenue from sales (calculated as `qty * unit_price`)

---

## 🧠 Model Used

- **Model**: `DecisionTreeRegressor` from `scikit-learn`
- **Why this model**: 
  - Easy to interpret
  - Captures non-linear relationships
  - No need for feature scaling
  - Performs well with small- to medium-sized datasets

---

## ⚙️ How it Works

```python
from sklearn.tree import DecisionTreeRegressor

# Feature and target separation
X = retail_price[['qty', 'unit_price', 'comp_1', 'product_score', 'comp_price_diff']]
y = retail_price['total_price']

# Initialize and train model
model = DecisionTreeRegressor()
model.fit(X, y)
```

Once trained, the model can be used to predict the total revenue given new data with similar features.


```python

---

## 📦 Dataset

The dataset includes essential pricing and competitive features. You can use your own CSV or explore public retail datasets from Kaggle or other sources.

---

## 🚀 How to Run

1. Open the notebook in Jupyter or Kaggle
2. Make sure all necessary libraries are installed (pandas, sklearn, seaborn, matplotlib)
3. Run all cells to:
   - Clean and explore the dataset
   - Train the model
   - Visualize insights

---

## 💡 Future Improvements

- Use ensemble models (like Random Forest or XGBoost) for better accuracy
- Add time-based features (e.g., month, season)
- Deploy the model using Gradio or Streamlit
- Perform hyperparameter tuning with `GridSearchCV`

---

## 📬 Contact

For questions or suggestions, feel free to reach out or open an issue.

---

Let me know if you'd like this in a downloadable `README.md` file or if you'd like to add Gradio deployment instructions later!
