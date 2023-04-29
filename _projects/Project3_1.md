---
name: Project 3.1
tools: [Python, HTML, vega-lite, ALTAIR]
image: assets/pngs/Project3_screenshot.png
description: This is the Final Project 3.1 by Shruti, Nidhi, Ketan
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
## Project 3.1

Final Project 3.1 published by Shruti Deekshitula, Nidhi Yadav and Ketan Mahajan


<h2> How much is US actually spending on food imports? </h2>
<!-- <h5> Published by: Nidhi Yadav, Ketan Mahajan, Shruti Deekshitula </h5> -->

<h3> Introduction </h3>

U.S. consumers demand variety, quality, and convenience in the foods they consume. As America is becoming more ethnically diverse, the food basket reflects a growing share of tropical products, spices, and imported gourmet products. Seasonal and climatic factors drive U.S. imports of popular types of fruits and vegetables and tropical products, such as cocoa and coffee. In addition, a growing share of U.S. imports can be attributed to intra-industry trade, whereby agricultural-processing industries based in the United States carry out certain processing steps offshore and import products at different levels of processing from their subsidiaries in foreign markets.

This data set provides import values of edible products (food and beverages) entering U.S. ports and their origin of shipment. Data are from the U.S. Department of Commerce, U.S. Census Bureau. Food and beverage import values are compiled by calendar year into food groups corresponding to major commodities or level of processing. 

The dataset summarizes annual food imports, values and volume by food category and source country, and is provided for the year 1999-2022 to enable users to track long-term growth patterns for food imports in the US.

<h3> Dataset Description </h3>

To begin with, the food commodities are segregated into various sub-categories like Food, Total foods etc. which are further classified into various categories like Animals, Beverages, Cocoa to name a few. The dataset contains 8 columns, 
with 5 (Commodity, Country, UOM, Category, Subcategory) being categorical and the remaining 3 (RowNumber, YearNum, FoodValue) being numerical variables. The variables which we have used throughout for our analysis are Commodity, Country, Category, Subcategory, YearNum and FoodValue.

Our group decided to focus our analysis on identifying food import trends in the US from respective countries for various commodities belonging to different categories and subcategories in terms of the food value in million dollars. To begin with, we preprocessed the data set to filter the data only for the countries and removed all the rows containing the cumulative food value for WORLD and food quantity in metric ton represented by WORLD (Quantity).

<h3> Analysis </h3>


To represent our analysis and derive insights we have created two interactive visualizations represented by a bar plot and a multi-line plot. For bar plot, the data is aggregated based on the food commodities belonging to the selected category to show aggregated food values. For multi-line plot, the preprocessed dataset is converted into a pivot table with index as the countries and columns as the years for which food has been imported to the US.

The first step for the user to interact with the charts is to select a category from the dropdown (for example:  animals, fish etc.), which will generate the bar plot. The bar plot will display the value bifurcated by commodities that are present in the category selected from the dropdown on the x-axis and corresponding food value in million $ on the y-axis. The user can further interact with this plot by clicking on a bar which will select the commodity represented by that bar. The multi-line plot takes the selected commodity as input and gets updated to show the import value for each country over a time series for the years 1999-2022.


<vegachart schema-url="{{ site.baseurl }}/assets/json/project3_chart.json" style="width: 100%"></vegachart>
<br />
<br />


<h3> Contextual Data </h3>

The first contextual data display shows the food imports comparision of United states and India.


<iframe src="https://data.worldbank.org/share/widget?end=2021&indicators=TM.VAL.FOOD.ZS.UN&locations=IN-US&start=1962&view=chart" width='700' height='500' frameBorder='0' scrolling="no" ></iframe>
<!-- ![Import USA vs India ](/assets/pngs/import_usa_india.PNG) -->

The second contextual data display shows the food imports comparision of United states and China, this vizualisation shows
the imports in a geographical distrubiton where we can see the countries on the map.

<iframe src="https://data.worldbank.org/share/widget?end=2021&indicators=TM.VAL.FOOD.ZS.UN&locations=US-CN&start=1962&view=map" width='700' height='500' frameBorder='0' scrolling="no" ></iframe>
<!-- ![Import USA vs China ](/assets/pngs/import_usa_china.PNG) -->



<h3> References: </h3>
- <https://data.worldbank.org/indicator/TM.VAL.FOOD.ZS.UN?end=2021&locations=IN&start=1962&view=chart>
- <https://www.ers.usda.gov/data-products/u-s-food-imports/>
- <https://altair-viz.github.io/>


<div class="left">
{% include elements/button.html link="https://github.com/ketan96-m/dataviz/blob/main/FoodImports.csv" text="Food Imports Dataset" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/ketan96-m/dataviz/blob/main/Group11_finalproject_part3.ipynb" text="Group11_Project3" %}
</div>