# 🛒 E-Commerce User Behavior & Retention Analysis

## 📌 Project Overview

This project analyzes user behavior in an e-commerce setting using real-world datasets. The goal is to understand how users interact with the platform, what drives conversions, and how operational factors like delivery time impact customer satisfaction.

The analysis combines:

* **User session behavior (RetailRocket dataset)**
* **Order, delivery, and review data (Olist dataset)**

---

## 🎯 Objectives

* Analyze user journeys from browsing to purchase (Funnel Analysis)
* Measure the impact of delivery time on return rates
* Explore customer behavior through sessions and interactions
* Generate actionable business insights

---

## 📂 Datasets Used

### 1. RetailRocket Dataset

* User interaction events (views, cart, purchases)
* Session-level behavior tracking

### 2. Olist E-Commerce Dataset

* Orders and order items
* Delivery timestamps
* Customer reviews (used as proxy for returns)

---

## ⚙️ Key Features & Analysis

### 🔹 1. Sessionization

* Built user sessions using a 30-minute inactivity threshold
* Identified user browsing patterns and engagement levels

---

### 🔹 2. Funnel Analysis (User Journey)

Tracked user flow across key stages:

* **View → Add to Cart → Purchase**

📊 Metrics:

* Conversion rates between each stage
* Drop-off points in the funnel

💡 Insight:

* Significant drop-off between browsing and purchase stages indicates potential UX or pricing friction

---

### 🔹 3. Delivery Time Impact Analysis

📦 Created a `delivery_days` feature:

```python
delivery_days = delivery_date - order_date
```

Analyzed:

* **Return rate vs delivery time**
* Delivery delays and customer dissatisfaction

📊 Key Finding:

* Longer delivery times correlate with higher return rates
* Fast delivery significantly improves customer experience

---

### 🔹 4. Return Behavior Analysis

* Used review scores as a proxy for returns
* Flagged low ratings (≤2) as likely returns

💡 Insight:

* Poor customer experience is strongly linked to returns

---

## 📊 Visualizations

The project includes:

* Funnel bar charts (conversion stages)
* Delivery time vs return rate charts
* Distribution plots for delivery time

All visualizations are included in the notebook.

---

## 🧠 Key Insights

* 🚚 **Delivery speed is critical**
  Orders delivered late show significantly higher return rates

* 🛍️ **Major drop-off in funnel**
  Many users browse but don’t convert → optimization opportunity

* ⭐ **Customer experience drives retention**
  Poor reviews strongly correlate with negative outcomes

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/ecommerce-analysis.git
```

2. Open the notebook:

```bash
jupyter notebook
```

3. Run all cells to reproduce the analysis

---

## 📈 Future Improvements

* Add cohort-based retention analysis (with correct user mapping)
* Build predictive models for returns and churn
* Create an interactive dashboard (Streamlit / Power BI)

