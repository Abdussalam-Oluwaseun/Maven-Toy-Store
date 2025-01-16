# Maven-Toy-Store
 A simple interactive KPI report to track key metrics and explore high-level trends
 
## Table of Content
* [Data Source](#data-source)
* [Tools](#tools)
* [Data Cleaning and Preparation](#data-cleaning-and-preparation)
* [Exploratory Analysis](#exploratory-analysis)
* [Data Analysis](#data-analysis)
* [Visualizaton](#visualizaton )
* [Insights](#insights)
* [Recommendations](#recommendations)
* [Conclusion](conclusion)

## Data Source
Maven Analytics
[Mavenanalytics.io](https://app.mavenanalytics.io/guided-projects/331595bf-f741-4894-b9c6-1c047c33e8ad)

## Tools
PowerBi

## Data Cleaning and Preparation
The dataset was analyzed using Power Query to identify and address any inconsistencies or errors.

## Exploratory Analysis
  Using Power Query, initial exploration of the dataset was conducted to find paterns and answer these questions 
  * What are the overall trends and total in revenue, orders, and profit over time?
  * Which products generate the most sales, units, and profit?
  * What is the distribution of orders across different product categories?
  * Which store location generates the most revenue or profit?
  * How does profit vary by month or quarter?
    
## Data Analysis
measures and calculated columns created to analize for analysis
``` DAX
Revenue = sales[Sale] * sales[Units]

Profit = sales[Revenue] - (sales[Cost] * sales[Units])

Avg revenue = AVERAGE(sales[Revenue])

Total Orders = DISTINCTCOUNT(sales[Sale_ID] )

Total Profit = SUM(sales[Profit])

Total Revenue = SUM(sales[Revenue] )
```
## Visualizaton 
the visualization was developed using PowerBi

[Report Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzU3ZGJkNDMtZTc3Mi00YzkyLWE2ODQtNGExNDVkZWEwOTAxIiwidCI6IjI2MTRhZTljLTQ2MmUtNDMyMi05MGE4LWRkMmNkYzYyM2ZjNiJ9)

![{70B745FF-C7AD-4EC0-A0D9-EC73A5EFBCAB}](https://github.com/user-attachments/assets/d05326b8-7029-4f18-a032-2ea65d028ecd)

![{A3CF107D-1368-4529-B4AF-117151A05E55}](https://github.com/user-attachments/assets/a26e5e91-5e61-4299-933f-592becad5594)

## Insights
The performance of the four store locations (Airport, Commercial, Downtown, and Residential) was evaluated based on revenue, profit, and units sold.

* Airport: The Airport location generated a total revenue of $1.29M, with a profit of $328.05K, and sold 68K units. The top products at this location were Lego Bricks, Color Buds, and Rubik's Cube.

* Commercial: The Commercial location recorded a higher revenue of $3.28M, a profit of $928.86K, and sold 185K units. The top products were consistent with the Airport location: Lego Bricks, Color Buds, and Rubik's Cube.

* Downtown: The Downtown store was the best-performing location, generating a total revenue of $8.22M with a profit of $2.25M and selling 480K units. The top products at this location were Lego Bricks, Color Buds, and Action Figure.

* Residential: The Residential location generated a revenue of $1.66M, with a profit of $460.39K, and sold 96K units. The top products here were Lego Bricks, Color Buds, and Action Figures.
  
Top-Performing Location: The Downtown store generated the highest revenue ($8.22M), profit ($2.25M), and sales volume (480K units).
Least-Performing Location: The Airport store recorded the lowest revenue ($1.29M) and profit ($328.05K).
Top Products Across Locations: Lego Bricks and Color Buds consistently ranked as the most sold and profitable products in all store locations.

## Recomendations
* Leverage the strong performance of the Downtown store by replicating its strategies (e.g., product selection, promotions) in other locations.
* Increase marketing efforts and inventory in December to capitalize on holiday demand, especially for the Toys category.
* Develop targeted strategies to improve sales and profit at the Airport and Residential stores, such as offering discounts or promoting high-performing products.
* While Toys dominate, consider promoting other categories like Games and Art & Crafts in top-performing locations to diversify revenue streams.

## Conclusion
This analysis highlights the strengths of the Downtown store, the dominance of the Toys category, and the significance of seasonal demand in December. Addressing underperforming locations, capitalizing on high-demand periods, and diversifying product focus are essential to sustaining and improving sales performance across all stores.

