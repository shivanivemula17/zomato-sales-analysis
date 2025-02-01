# zomato-sales-analysis
This repository contains a Zomato Sales Analysis project, focusing on data cleaning, exploratory data analysis (EDA), and visualization.
# 🍽️ Zomato Sales Analysis  

## 📌 Project Overview  
This project analyzes **Zomato sales data** to uncover **customer preferences, restaurant performance, order trends, and revenue insights**. The goal is to understand how different factors affect sales and help restaurants optimize their offerings.  

## 🔍 Key Features  
✔️ **Cleaned & pre-processed the dataset** to remove inconsistencies and missing values.  
✔️ **Performed Exploratory Data Analysis (EDA)** to discover trends in orders, ratings, and revenue.  
✔️ **Created data visualizations** using **Matplotlib & Seaborn** for better insights.  
✔️ **Analyzed key factors such as:**  
   - Most popular restaurants and cuisines.  
   - Customer spending behavior.  
   - Impact of restaurant ratings on sales.  
   - Order frequency and delivery trends.  

## 🛠️ Technologies Used  
- **Python**  
- **Pandas** (for data cleaning & analysis)  
- **Matplotlib & Seaborn** (for visualization)  
- **NumPy**  
- **Jupyter Notebook**  

## 📊 Sample Analysis  
### 🔹 1. Most Popular Cuisines Ordered  
```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd

# Load dataset
df = pd.read_csv("zomato_sales_data.csv")

# Count most popular cuisines
cuisine_counts = df['Cuisines'].value_counts().head(10)

# Plot top cuisines
plt.figure(figsize=(10,5))
sns.barplot(x=cuisine_counts.index, y=cuisine_counts.values, palette="coolwarm")
plt.title("Top 10 Most Ordered Cuisines on Zomato")
plt.xlabel("Cuisines")
plt.ylabel("Number of Orders")
plt.xticks(rotation=45)
plt.show()
