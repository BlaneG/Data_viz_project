# Data_viz_project

## Summary

Check out a the visualization I created for this project using D3.js [here](https://htmlpreview.github.io/?https://github.com/BlaneG/Data_viz_project/blob/master/index_5-change_to_chloropleth.html) (may take a few seconds to load, and javascipt may be blocked if visualization does not fully load).

This visualization answers the question:  who in American is using peer to peer lending.  It uses a coloured map (a chloropleth) to show which states are using peer-to-peer loans (dollars per capita) over a period of roughly 10 years using data from Prosper Marketplace.  Prosper is a peer to peer lending site that connects individual borrowers with lenders.  It's a more formal approach to lending operating outside of the traditional bank credit market.  The Prosper dataset provides a rich set of information about individual loans distributed in the US.  Given the state level geographic labels provided for individual loans, the dataset provides many opportunities for visualizing the data with maps. Key outliers in the dataset include DC ($6.43 in cumulative, per capita loans distributed) as well as ND, IA, MD ($0.32-0.37 in cumulative, per capita loans distributed).  

This data viz project was put together for completion of Udacity's data visualization course.  The dataset is made available by [Prosper](https://www.prosper.com/) and includes 81 variables (e.g. loan amount, interest rate, etc.) for over 100,000 peer-to-peer loans in the US.   

## Design

The aim of this visualization was to illustrate the cumulative, per capita value of loans distributed to each state spanning the temporal bounds of the dataset (November 15th, 2005 - March 12th, 2014).  A chloropleth map was used to illustrate the findings with the darker states having borrowed more money per capita over the time horizon.  By hovering over each bubble with the mouse, a textbox can is activated displaying the numerical data for each state.  Outliers in the data are labelled.

## Feedback
Feedback from early iterations incorprated into the visualization included:

1) An early iteration of the data visualization explored use of a bubble map to display the data. It was pointed out that some of the smaller bubbles were originally hidden beneath large bubbles and the hover functionality to display data wasn't working for these smaller hidden bubbles.  The data was sorted to layer the smallest bubble plots on top so overlapping large bubbles wouldn't obscure smaller bubbles.

2) The bubble plot originally displayed the cumulative loans distributed to each state.  It was suggested that the bubbles be scaled based on the population of each state to illustrate differences in per capita loans distributed to residents in each state.

3) A lot of the bubbles look like they are a similar size.  Does this plot really tell us anything interesting? 
   -a bar chart was added below the map to help illustrate differences in cumulative, per capita loans distributed to residents within each state.
   
4) A chloropleth would be more useful to avoid overplotting in the Northeast.

## Resources
The following resources we used to implement the visualizations for this project:

* Maps:

   - Responsive maps with D3 - http://eyeseast.github.io/visible-data/2013/08/26/responsive-d3/
   - US shapefiles - http://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html
   - Converting shapefile to geoJSON - http://ogre.adc4gis.com/
   - Let's make a bubble map - http://bost.ocks.org/mike/bubble-map/
   - Understanding geopaths - https://github.com/mbostock/d3/wiki/Geo-Paths
   - d3 geo projections - https://github.com/mbostock/d3/wiki/Geo-Projections
   - d3 geo projections - https://github.com/mbostock/d3/wiki/Geo-Projections
   - tooltips to display data - http://stackoverflow.com/questions/10805184/d3-show-data-on-mouseover-of-circle
   - highlighting states on mouseover with css - http://bl.ocks.org/ericcoopey/ff45f603352fb7475c85

* Charting:

   - responsive charts with D3 - http://eyeseast.github.io/visible-data/2013/08/28/responsive-charts-with-d3/
   - a bar chart - http://bl.ocks.org/mbostock/1389927#index.html

* Legends:
   - http://d3-legend.susielu.com/

* Data wrangling:

   - D3 nest tutorial - http://bl.ocks.org/phoebebright/raw/3176159/
   - Sorting objects, arrays, etc. in Javascript - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort
   - Formatting numbers - http://bl.ocks.org/zanarmstrong/05c1e95bf7aa16c4768e
