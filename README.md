# Data_viz_project
##Summary
This data viz project is a work in progress to fulfill requirements of Udacity's data visualization course.  The dataset is made available by [Prosper](https://www.prosper.com/) and includes 81 variables (e.g. loan amount, interest rate, etc.) for over 100,000 peer-to-peer loans.  

####Next steps:

* - [ ] convert bubble to pie charts for each state 
    * - [ ] size of pie chart represents total LoanOriginalAmount by state
    * - [ ] pie slices representing the fraction of LoanOriginalAmount by CreditGrade
* - [ ] Make the map a chloropleth representing DebtToIncomeRatio

##Design
Prosper is a peer to peer lending operation that helps to connect individual borrowers with lenders.  It's a more formal approach to lending operating outside of the traditional bank credit market.  The Prosper dataset provides a rich set of information about individual loans distributed in the US.  Given the state level geographic labels provided for individual loans, the dataset provides many opportunities for visually exploring variability across geographic regions.  

The aim of this visualization was to explore the cumulative, value of loans distributed within each state - spanning the temporal bounds of the dataset (November 15th, 2005 - March 12th, 2014) - using a bubble plot.  One bubble is used with the area of the bubble equal to the square root of the cumulative loan amount.  When using bubbles, it is important to scale the size of the bubble to the square root of the parameter you are plotting because the radius is used to format bubble size, and the area of a circle is proportional to it's radius<sup>2</sup>.  The transparency of each bubble is set to 50% in order to add some emphasis to overlapping data.  A textbox can be activated for each bubble to display the state and cumulative loan amount for that state by hovering the over each bubble with the mouse.

##Feedback
Feedback from early iterations for the visualization that were incorporated in the final project included:
1) Move the smallest data points to the front of the map so overlapping large bubbles don't obscure smaller bubbles
2) Scale the total loan value to per capita total loan value for each state so we can see the difference in per capita loan value for each state.
3) 

##Resources
The following resources we used to implement the visualizations for this project:

* d3 projections - https://github.com/mbostock/d3/wiki/Geo-Projections
* pie layout - https://github.com/mbostock/d3/wiki/Pie-Layout
* US shapefiles - http://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html
* Converting shapefile to geoJSON - http://ogre.adc4gis.com/
* Let's make a bubble map - http://bost.ocks.org/mike/bubble-map/
* Understanding geopaths - https://github.com/mbostock/d3/wiki/Geo-Paths
* D3 nest tutorial - http://bl.ocks.org/phoebebright/raw/3176159/
* Sorting objects, arrays, etc. in Javascript - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort
