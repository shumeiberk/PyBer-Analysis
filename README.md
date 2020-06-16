# PyBer-Analysis
## Challenge Overview

Technical Analysis Deliverable 1: A DataFrame that summarizes the key metrics for the ride-sharing data by city type.
Technical Analysis Deliverable 2: A multiple-line chart, with one line for each city type, that shows the sum of the fares for each week.
Delivering Results: A written report of your results, saved in a README.md document on your GitHub repository.


# Resources
Data Source: city_data.csv, ride_data.csv
Software: Python 3.6.1, Jupyter Notebook 6.0.1

# Challenge Results

The purpose of this analysis is to dig deeper into the frequency and fare metrics of each city type so the PyBer CEO can understand the ridership dynamic between urban, rural and suburban segments. 
The pyber data was merged between the city and ride data files and the fares, drivers and rides were calculated to assess the totals and  averages across all city types.  Specific data was also filtered out so that the individual metrics by driver count and fare totals can be grouped together for the data setup and cleaning. 
As seen in the below summary, the highest volume of rides & drivers is in the urban cities while lowest volume of rides & drivers are in the rural cities; but the highest fares and most lucrative fares for a driver is in the rural cities (although with less frequency). 
![City_Type_Dataframe](https://github.com/shumeiberk/PyBer-Analysis/blob/master/City_Type_Dataframe.JPG)
If we just look at the weekly trends across the city types from Jan to April 2019, we can see that across almost all city types the peak ridership occurs end of Feb.  Urban and Suburban cities from Jan-Feb has an increase in riderhsip while there's a lull in the rural cities, in contrast rural cities increase ridership from Mar-Apr while urban cities is declining and suburban area is relatively flat.
![Challenge_Fare_Summary](https://github.com/shumeiberk/PyBer-Analysis/blob/master/Challenge_Fare_Summary.png)

The challenges with the technical challenge in merging the city and fare data is that metrics can be duplicated, for example rider_count is duplicated for each city line item and date so you need to sum the unique driver_counts by city type without dupes.  For the line graph you also want to make sure that the data datetime type is set up and correct which can be reset through the index.

There are obvious logical disparties for the different city types.  The highest volume in fares and drivers is in urban cities because populations are always higher in urban centers because of density, while rural cities are more spread out.  There are more paid ridership in urban cities because less people own cars while most rural areas people drive their own cars.  To improve on potential sales by increasing ridership would depend on digging into the data deeper.  Recommendations for further analysis is to understand whether there are any specific reasons for the trends seen for the various city types.  For example, why is there an increase in ridership for urban and suburban cities while rural dips from Jan-Feb?  Is there a difference during holidays or seasonality? Are there certain cities where there are outliers in fares or drivers?  This can be done by extending the current data for the whole year and using the stats module from SciPy to break down the data across all three cities and visualize in box and whisker charts as well as a scatter plot. 

