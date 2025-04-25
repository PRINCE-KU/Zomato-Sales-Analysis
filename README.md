
<p align="center">
  <img src="https://img.freepik.com/free-vector/data-analytics-concept-illustration_114360-917.jpg" width="70%" alt="Data Analysis Banner"/>
</p>

<h1 align="center">🍽️ Zomato Data Analysis & Recommendation System</h1>

<p align="center">
  <strong>📊 Built using Power BI & Excel | 📍 Location-based Food Insights | ⭐ Ratings & Recommendation Engine</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PowerBI-Dashboard-yellow?style=for-the-badge&logo=powerbi" />
  <img src="https://img.shields.io/badge/Excel-Analysis-green?style=for-the-badge&logo=microsoft-excel" />
  <img src="https://img.shields.io/badge/Visualization-Storytelling-blue?style=for-the-badge&logo=plotly" />
</p>

---
![Capture](https://github.com/user-attachments/assets/a8cb51c6-1964-4020-8500-2ce69ede17f0)


## 🧠 Project Context

The food delivery industry has experienced massive growth in recent years, and platforms like Zomato play a crucial role in shaping user choices. This project is aimed at analyzing Zomato's dataset to uncover valuable business insights that can help:

- Understand restaurant distribution and availability across cities
- Identify popular cuisines and high-rated restaurants
- Analyze customer rating patterns and pricing trends
- Build a basic **recommendation logic** based on user preferences

Using **Power BI** for interactive dashboards and **Excel** for quick summaries, this project turns raw food data into actionable decisions for customers, restaurant owners, and investors.

---
## 🚀 Key Features

🔍 **Restaurant Search & Filtering**  
Easily explore restaurants based on location, cuisine, rating, and price range.

📍 **City-wise Restaurant Analysis**  
Visualize how restaurants are distributed across major cities like Delhi, Bangalore, Kolkata, etc.

⭐ **Rating Trends**  
Analyze customer ratings to find the best-rated restaurants and understand customer satisfaction.

🍕 **Cuisine Popularity**  
Identify the most loved cuisines in different cities and discover food trends.

📈 **Price vs Rating Correlation**  
Understand whether higher prices actually mean better food and service.

🔄 **Interactive Dashboards (Power BI)**  
Fully interactive charts and visuals that update based on filters for a dynamic user experience.

📊 **Excel Summary Reports**  
Quick summaries and pivot tables for basic analysis and understanding.

🤖 **Recommendation Logic** (basic)  
Suggests restaurants based on rating, votes, and user preferences using rule-based filtering.

## 📷 Dashboard Screenshots

Here’s a glimpse of the interactive dashboards created using Power BI and Excel 👇



### 🔶 Power BI Dashboard – Overview



![Capture](https://github.com/user-attachments/assets/778b26a2-e5f2-4ec1-84d4-8393ef5c09f9)
## 📝 Project Overview

Welcome to a visual feast of Zomato Data Analysis & Recommendation System! 🍽️  
This Zomato Data Analysis project dives into the heart of India's food scene. From spicy North Indian dishes to sizzling fast food trends, we’ve decoded what the crowd really craves — all with the magic of **Power BI** and **Excel Dashboards**. 

Get ready to explore city-wise restaurant insights, pricing patterns, and what makes a restaurant truly “5-star”! ⭐  
Whether you're a foodie, a data nerd, or a future business leader — this dashboard has a bite for everyone!





### 🟢 Power BI Dashboard – City-wise Restaurant Distribution




![Capture3](https://github.com/user-attachments/assets/7aae52e3-69a5-4a88-af37-1a8f8b2749c6)
## 🏙️ City-wise Restaurant Distribution

In this section, we analyze the **distribution of restaurants** across major Indian cities. The data reveals how restaurants are spread out and highlights the concentration of restaurant activity in different metropolitan areas.

### Key Insights:
- **Delhi NCR** has the highest number of listed restaurants, making it the food hub of India.
- **Bangalore** follows closely, with a large concentration of restaurants catering to diverse cuisines.
- **Mumbai** and **Kolkata** show a balanced spread across various types of restaurants, with a higher preference for **fine dining** and **fast food** outlets.
- Smaller cities like **Chennai** and **Pune** have a growing restaurant scene, with an increasing demand for fast food and local cuisines.

### Visual Representation:
The **Power BI dashboard** provides an interactive map and bar chart for a city-wise breakdown, helping users visually explore restaurant densities and types across different locations.

---

### City Distribution Highlights:
1. **Delhi NCR** - Dominates with over **30%** of the total restaurants in the dataset.
2. **Bangalore** - The second-largest city with an expanding food culture.
3. **Mumbai** - Known for its rich food diversity, including **fast food**, **cafes**, and **international cuisine**.
4. **Kolkata** - Popular for **local Bengali cuisine** and an increasing number of **street food vendors**.






### 🧾 Power BI Dashboard - User Performance:



![Capture2](https://github.com/user-attachments/assets/c6b70271-a5f4-4b33-b83a-326f1c09f6f2)

1. Revenue per Restaurant (Within a Column)
To calculate Revenue per Restaurant in a single column, you would want to use a calculated column or field that divides the total revenue by the number of restaurants.

Power BI (DAX Formula):
In Power BI, you can use a Calculated Column to add a column that shows the Revenue per Restaurant.

Go to the Data view in Power BI.

Click on the New Column button in the Modeling tab.

Use this DAX formula to create the Revenue per Restaurant column:

dax
Copy
Edit
RevenuePerRestaurant = 
DIVIDE(ZomatoData[Revenue], ZomatoData[RestaurantCount], 0)
This formula divides the Revenue by the Restaurant Count for each city. The DIVIDE function safely handles division by zero.

Excel (Formula Example):
If you're using Excel, you can create a new column to calculate Revenue per Restaurant.

In a new column (let's say Column D), enter the following formula:

excel
Copy
Edit
=IF(B2<>0, C2/B2, 0)
Where:

B2 is the column containing Restaurant Count.

C2 is the column containing Revenue.

This formula divides Revenue by Restaurant Count. If the count is zero, it returns 0 to avoid errors.

2. Restaurant Growth Rate (Within a Column)
If you want to analyze Restaurant Growth Rate (i.e., how the number of restaurants grows over time) within a single column, you can calculate the percentage change year-over-year (YoY) or month-over-month (MoM).

Power BI (DAX Formula for YoY Growth):
In Power BI, use a Calculated Column to compute the Restaurant Growth Rate from one year to another.

Go to the Data view in Power BI.

Click New Column.

Use the following DAX formula:

dax
Copy
Edit
RestaurantGrowthRate = 
VAR CurrentYear = YEAR(ZomatoData[Date])
VAR PreviousYear = YEAR(DATEADD(ZomatoData[Date], -1, YEAR))
VAR CurrentCount = CALCULATE(COUNT(ZomatoData[RestaurantName]), YEAR(ZomatoData[Date]) = CurrentYear)
VAR PreviousCount = CALCULATE(COUNT(ZomatoData[RestaurantName]), YEAR(ZomatoData[Date]) = PreviousYear)
RETURN IF(PreviousCount <> 0, (CurrentCount - PreviousCount) / PreviousCount, 0)
This formula calculates the growth rate of restaurants by comparing the restaurant count in the current year with the previous year.

Excel (Formula for Growth Rate):
In Excel, to calculate Growth Rate between two years:

In a new column (say Column E), enter the following formula:

excel
Copy
Edit
=IF(B3<>0, (B2-B3)/B3, 0)
Where:

B2 is the restaurant count for the current year.

B3 is the restaurant count for the previous year.

This formula calculates the percentage growth between two years for each city or each restaurant group.

3. Average Rating per City (Within a Column)
To analyze average ratings per city within a single column, you can calculate the average rating for each restaurant in a city.

Power BI (DAX Formula for Average Rating):
In Power BI, you can create a Calculated Column to show the average rating for each restaurant by city.

Go to Data view and click New Column.

Use this DAX formula:

dax
Copy
Edit
AvgRatingPerCity = 
CALCULATE(AVERAGE(ZomatoData[Rating]), ZomatoData[City] = EARLIER(ZomatoData[City]))
This formula calculates the average rating for restaurants within each city.

Excel (Formula for Average Rating):
In Excel, you can use the AVERAGEIF function to calculate the average rating for each city.

In a new column, say Column F, use this formula:

excel
Copy
Edit
=AVERAGEIF(A:A, A2, C:C)
Where:

A:A is the column containing the City.

A2 is the city for which you want to calculate the average.

C:C is the column containing the Ratings.

This formula calculates the average rating for each city by using the AVERAGEIF function.

4. Insights Derivation:
You can deriving insights from these columns to understand:

Which city has the highest Revenue per Restaurant or Restaurant Growth Rate.

Which city has the highest average rating and whether it corresponds to a higher number of restaurants or a specific cuisine.

For example, you can now:

Filter or sort by Revenue per Restaurant to see which cities perform the best.

Track the growth rate of restaurants in each city over the last few years.

Visualize the average ratings to see if cities with high restaurant counts are maintaining high quality.





## ⚙️ Tools Used

### 1. **Power BI**
   - **Usage**: Power BI was used to create interactive dashboards that allowed for in-depth data visualization and dynamic exploration of the restaurant dataset. The tool enabled quick insights into key metrics like ratings, cuisines, city-wise restaurant distribution, and price trends.
   - **Key Features**:
     - **Data Transformation**: Cleaned and reshaped raw data for better analysis.
     - **Interactive Visualizations**: Created dynamic charts like bar charts, pie charts, and heat maps for exploring the dataset visually.
     - **Slicers and Filters**: Enabled dynamic filtering for users to drill down by city, cuisine, rating, and price.
     - **Storytelling**: Developed a compelling data story with visuals that communicated the insights effectively.

### 2. **Microsoft Excel**
   - **Usage**: Excel was used for initial data cleaning, quick analysis, and generating summary reports. It was an essential tool for creating pivot tables, conditional formatting, and basic visualizations for exploratory data analysis.
   - **Key Features**:
     - **Data Cleaning**: Handled missing values, duplicates, and formatting issues using built-in Excel functions.
     - **Pivot Tables**: Used pivot tables to summarize restaurant data and perform quick calculations like average price, ratings, and votes.
     - **Charts and Graphs**: Created bar charts, line graphs, and pie charts to visually present trends like ratings vs. price or cuisine popularity.
     - **Conditional Formatting**: Highlighted key data points like high ratings or top-rated cuisines for easy identification.

## 📂 Folder Structure

Here’s an overview of the folder structure for the Zomato Data Analysis project:

Zomato-Data-Analysis/ │ ├── data/
│ ├── zomato_data.csv # Raw dataset containing restaurant information, ratings, etc. │ └── cleaned_data.csv # Cleaned dataset after preprocessing │ ├── images/
│ ├── powerbi_overview.png # Screenshot of the Power BI dashboard overview │ ├── city_wise_distribution.png # City-wise restaurant distribution (Power BI) │ └── excel_summary.png # Screenshot of Excel summary (Pivot Table & Charts) │ ├── notebooks/
│ └── data_cleaning.py # Python script for cleaning and preprocessing data (if applicable) │ ├── powerbi_reports/
│ ├── zomato_dashboard.pbix # Power BI report file with all dashboards │ └── README.md # Project overview, setup, and usage instructions


## 📜 Conclusion

This **Zomato Data Analysis & Recommendation System** project provides valuable insights into restaurant trends, customer preferences, and pricing patterns across various Indian cities. By leveraging **Power BI** for interactive dashboards and **Excel** for quick summaries, we were able to uncover the most popular cuisines, top-rated restaurants, and price correlations with customer ratings.

### Key Takeaways:
- **City-wise Distribution**: Major cities like Delhi NCR and Bangalore dominate the restaurant market.
- **Cuisine Preferences**: North Indian cuisine is the most popular, followed closely by Chinese and Italian.
- **Ratings & Price Correlation**: Higher prices don't necessarily mean better ratings; many budget-friendly restaurants are highly rated.
- **Restaurant Type Trends**: Delivery services are growing in popularity over dine-in services, especially in metro cities.

### Future Improvements:
- **Advanced Recommendation System**: Incorporating machine learning algorithms to suggest restaurants based on user preferences and past ratings.
- **Real-Time Data**: Integrating real-time data from the Zomato API for up-to-date restaurant information.
- **User Feedback Integration**: Adding a feature to collect and analyze user reviews for personalized recommendations.

This project has laid the foundation for a more sophisticated restaurant recommendation system that can benefit both customers and restaurant owners by providing data-driven insights and decisions.





