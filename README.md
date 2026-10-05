# 🛒 Blinkit Sales Analysis

Exploratory data analysis of **13,000 Blinkit products** covering sales, pricing, discounts, delivery performance, and city-level trends, built with Python, Pandas, Seaborn, and Plotly.



![Python](https://img.shields.io/badge/Python-3.x-blue)




![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)




![Plotly](https://img.shields.io/badge/Plotly-Visualization-orange)




![Status](https://img.shields.io/badge/Status-Completed-brightgreen)



---

## 📌 Project Overview

Quick-commerce platforms like Blinkit depend on fast delivery, smart pricing, and accurate demand forecasting. This project analyses product-level data to understand what drives sales, how discounts and offers perform, and how delivery times vary across cities.

## 🎯 Objectives

- Clean and prepare the raw dataset for analysis
- Identify top-performing categories, brands, and cities
- Evaluate the impact of discounts and offer types on sales and profit
- Analyse delivery time and delivery status across cities
- Uncover the key drivers of product demand

## 📂 Dataset

- **Rows:** 13,000 products
- **Columns:** 25

| Group | Columns |
|-------|---------|
| Product | `product_id`, `product_name`, `category`, `brand`, `seller`, `packaging_type`, `weight_g`, `is_organic` |
| Pricing | `price`, `discount_pct`, `final_price`, `profit_margin_pct`, `offer_type` |
| Performance | `rating`, `num_reviews`, `sold_quantity`, `stock`, `reorder_level`, `demand_index` |
| Logistics | `city`, `delivery_time_min`, `delivery_status` |
| Dates | `date_added`, `expiry_date`, `shelf_life_days` |

## 🧹 Data Cleaning

- Checked for duplicate rows (none found)
- Filled missing `offer_type` values with `"No Offer"` (about 50% of rows)
- Converted `date_added` and `expiry_date` to datetime
- Validated prices, ratings, discounts, stock, sales, and delivery times for invalid values
- Saved the cleaned data as `blinkit_cleaned.csv`

## 📊 Key Insights

- **Sales are evenly spread across categories.** Bakery, Grocery, Personal Care, and Dairy each sold about 270K units, so no single category dominates.
- **Mumbai leads city sales** (about 220K units), followed closely by Bengaluru and Delhi.
- **Delivery speed varies widely by city.** Pune is fastest (about 21.5 min average) while Lucknow is slowest (about 34.5 min).
- **About 20% of orders are delayed**, and 80% arrive on time.
- **Demand index is the strongest sales driver** (correlation of about 0.91 with units sold).
- **Discounts show little impact on sales or margin.** Higher discount levels did not produce consistently higher volumes.
- **Britannia is the top-selling brand** by total units sold.

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Plotly
- **Environment:** Jupyter Notebook / Google Colab

## 📁 Repository Structure

```
blinkit-sales-analysis/
├── blinkit_sales_analysis.ipynb   # Main analysis notebook
├── blinkit_dataset.csv            # Raw dataset
├── blinkit_cleaned.csv            # Cleaned dataset
├── requirements.txt               # Dependencies
└── README.md
```

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/blinkit-sales-analysis.git
cd blinkit-sales-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook blinkit_sales_analysis.ipynb
```

## 💡 Recommendations

- Prioritise logistics improvements in slower cities such as Lucknow and Jaipur
- Use demand index for inventory planning and stock replenishment
- Re-evaluate blanket discounting, since it shows weak returns on volume
- Reduce delayed deliveries to improve customer experience

## 👤 Author

**Arpan Ghosal**
[LinkedIn](https://www.linkedin.com/in/arpan-ghosal-15a430338/?isSelfProfile=true) · [GitHub](https://github.com/PyInsightHub)

---
⭐ If you found this project useful, consider giving it a star!
