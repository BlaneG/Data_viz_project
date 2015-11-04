# Data_viz_project
##Summary
This visualization explores the cumulative, per capita loans distributed for each state over a period of about 10 years.  The data is displayed using a bubble plot and bar chart for each state.  The plot illustrates which states are the biggest users of peer to peer lending through Prosper.  Prosper is a peer to peer lending operation that helps to connect individual borrowers with lenders.  It's a more formal approach to lending operating outside of the traditional bank credit market.  The Prosper dataset provides a rich set of information about individual loans distributed in the US.  Given the state level geographic labels provided for individual loans, the dataset provides many opportunities for visually exploring variability across geographic regions. Key outliers in the dataset include DC ($6.43 in cumulative, per capita loans distributed) as well as ND, IA, MD ($0.32-0.37 in cumulative, per capita loans distributed).  

This data viz project was put together for completion of Udacity's data visualization course.  The dataset is made available by [Prosper](https://www.prosper.com/) and includes 81 variables (e.g. loan amount, interest rate, etc.) for over 100,000 peer-to-peer loans in the US.   

##Design

The aim of this visualization was to explore the cumulative, percapita value of loans distributed within each state - spanning the temporal bounds of the dataset (November 15th, 2005 - March 12th, 2014).  A map was used to illustrate geographic differences in per capita loan distributions using a bubble plot.  Data points in the upper and lower quartile are color coded with red and blue respectively while the interquartile range is color coded with a light grey.  A bar chart was added to help clarify differences in the magnitude of per capita loans distributed to each state which are more difficult to grasp from the bubble plot alone.  The area of each bubble is scaled to the square root of the cumulative, per capita loans distributed to residents of each state.  When using bubbles, it is important to scale the size of the bubble to the square root of the parameter you are plotting because the radius is used to format bubble size, and the area of a circle is proportional to it's radius<sup>2</sup>.  The transparency of each bubble is set to 50% which adds some emphasis to overlapping data.  By hovering over each bubble with the mouse, a textbox can is activated displaying the cumulative, per capita loan amount distributed within the state.

##Feedback
Feedback from early iterations incorprated into the visualization included:

1) It was pointed out that some of the smaller bubbles were originally hidden beneath large bubbles such that the hover functionality to display the data wasn't working for smaller bubbles.  The data was sorted to layer the smallest bubble plots on top so overlapping large bubbles wouldn't obscure smaller bubbles.

2) The bubble plot originally displayed the cumulative loans distributed to each state.  It was suggested that the bubbles be scaled based on the population of each state to illustrate differences in per capita loans distributed to residents in each state.

3) A lot of the bubbles look like they are a similar size.  Does this plot really tell us anything interesting? 
   -a bar chart was added below the map to help illustrate differences in cumulative, per capita loans distributed to residents within each state.

##Resources
The following resources we used to implement the visualizations for this project:

* Maps:

   - Responsive maps with D3 - http://eyeseast.github.io/visible-data/2013/08/26/responsive-d3/
   - US shapefiles - http://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html
   - Converting shapefile to geoJSON - http://ogre.adc4gis.com/
   - Let's make a bubble map - http://bost.ocks.org/mike/bubble-map/
   - Understanding geopaths - https://github.com/mbostock/d3/wiki/Geo-Paths
   - d3 geo projections - https://github.com/mbostock/d3/wiki/Geo-Projections

* Charting:

   - responsive charts with D3 - http://eyeseast.github.io/visible-data/2013/08/28/responsive-charts-with-d3/
   - a bar chart - http://bl.ocks.org/mbostock/1389927#index.html

* Legends:
   - http://d3-legend.susielu.com/

* Data wrangling:

   - D3 nest tutorial - http://bl.ocks.org/phoebebright/raw/3176159/
   - Sorting objects, arrays, etc. in Javascript - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort
   - Formatting numbers - http://bl.ocks.org/zanarmstrong/05c1e95bf7aa16c4768e
