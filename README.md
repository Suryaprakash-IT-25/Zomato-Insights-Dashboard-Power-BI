# 🍽️ Zomato Insights Dashboard – Power BI Project

This project is an end-to-end **Power BI analytics dashboard** built using Zomato restaurant data.  
The report provides actionable insights on **restaurant performance, cost trends, customer ratings, online delivery preferences, and cuisine popularity** across multiple cities.

---

## 📊 Project Overview

The **Zomato Insights Dashboard** helps stakeholders understand:

- Which cities have the highest number of restaurants  
- Rating distribution across locations  
- Average cost for two by city & cuisine  
- Online order impact on restaurant performance  
- Popular cuisines and top-performing restaurants  
- Restaurant type segmentation (Casual Dining, Café, Delivery, etc.)

This dashboard is ideal for **data analysis, business insights, and Power BI portfolio building**.

---

## 🧾 Key Features

### ✔️ Interactive Visuals:
- City-wise restaurant distribution  
- Rating analysis with detailed segmentation  
- Top cuisines & restaurant type breakdown  
- Average spending (Cost for Two) analysis  
- Online order vs. offline preference trends  

### ✔️ Data Cleaning & Transformation (Power Query):
- Removed duplicates  
- Standardized cuisine and city columns  
- Converted numerical columns  
- Handled missing values and categorical formatting  

### ✔️ Modeling:
- Star schema design  
- Relationship mapping  
- Custom calculated columns & DAX measures  

---

## 🛠️ Tools & Technologies Used

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **Data Modeling**
- **Zomato Dataset (.csv)**

---

## 🧮 DAX Measures Used

Some examples of the DAX measures implemented:

```DAX
Total Restaurants = COUNT(Retailer[RestaurantID])

Average Rating = AVERAGE(Restaurant[Rating])

Average Cost for Two = AVERAGE(Restaurant[Cost_for_Two])

Online Order % = 
DIVIDE(
    CALCULATE(COUNT(Restaurant[RestaurantID]), Restaurant[Online_Order] = "Yes"),
    COUNT(Restaurant[RestaurantID])
)

