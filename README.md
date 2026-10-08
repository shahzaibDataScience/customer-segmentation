# 👥 Customer Segmentation with K-Means

Group mall customers into segments using **K-Means clustering** (unsupervised learning), so marketing can target each group differently.

## What you'll learn

- What **unsupervised learning** is (no labels → no accuracy score)
- How **K-Means** works: pick k centers, assign points, repeat until stable
- The **elbow method** for choosing the number of clusters
- Why `random_state` and `n_init` matter for reproducible results
- How to **profile clusters** and turn them into business actions

## Dataset

`data/mall_customers.csv` — 2000 customers, generated with seed 42:

| Column | Meaning |
|---|---|
| CustomerID | unique customer id |
| Age | customer age |
| AnnualIncome_k | yearly income in thousands |
| SpendingScore | spending score 1–100 |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook customer_segmentation.ipynb
```

## Key findings

- The elbow method clearly suggests **k = 5** clusters
- 5 well-separated segments found, e.g. **premium targets** (young, high income, high spending 🎯) and **budget youngsters** (low income but high spending)
- Cluster sizes are balanced (~400 customers each)

## 🎓 Explain it yourself

1. What is the difference between supervised and unsupervised learning?
2. What is "inertia" in K-Means, and why does it always decrease as k grows?
3. What does the elbow method tell you, and why did we pick k = 5?
4. Why do we set `random_state=42` and `n_init=10`?
5. A new customer is 30 years old, income 90k, spending score 85 — which segment would they belong to, and what marketing would you suggest?
