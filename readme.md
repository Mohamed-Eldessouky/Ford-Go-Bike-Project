# Ford Go-Bike Project
## by Mohamed Elhussien Eldessouky


## Dataset

> The dataset has information about 1,154,202 individual rides made in Ford Gobike sharing system representing three major cities in USA (San Francisco, Boston and New York) during February 2019.

> The dataset was collected from the following links:
https://s3.amazonaws.com/hubway-data/index.html
https://s3.amazonaws.com/tripdata/index.html

> Data wrangling steps are summarized as following:
1- Merging the three data frames after dropping unnecessary columns and adding cities columns.
2- Limiting gender column to males and females only.
3- Removing null value rows.
4- Renaming columns for easier interpretation.
5- Calculating distance from longitudes and latitudes based on Haversine formula.
6- Converting stations id and birth year columns from float into integers.
7- Adding age column based on birth year column
8- Converting date-time columns from string into date-time format.
9- Extracting hours from date-time column.
10-Adding day of week column to determine whether the day is weekday or weekend.
11-Adding a new column for the duration in minutes.
12-Adding a new column to categorize trips into three categories bases on duration.

## Summary of Findings

> The duration histogram was highly skewed to the right, but after plotting the distribution on logarithmic scale, the data was found to be 
normally distributed around 9 minutes. Based on the distribution, the trips can be categorized into short trips (below 20 minutes), moderate trips (more than 20 minutes and less than 1 hour) and finally long trips (more than 1 hour). The interesting thing about trip categories is that although short trips represents the majority of trips with more than 87%, the sum of trips duration represents only 58.2% of all trips duration, on the other side, moderate and long trips which represents nearly 13% of all trips, their summation of trip duration is more than 40%, consequently moderate and long trips are as important as short trips. The distance distribution has nearly the same trend as duration, so the exploration focuses only on duration variable as an indication for distance. The histograms for trips distribution along day hours in both weekdays and weekends clearly shows the difference between both day types, where for the weekdays, there is a bimodal curve observed with the first peak around 8-9 am and the second peak around 5-6 pm which matches work arrival and departure times, second for the weekends, there is a complete different curve with only one peak around 2 pm with a gradual decrease before and after this time, The heat map of age vs day hours is very important in determining both the age of the target segment and the hours where the trips become at the peak, the main target segment in weekdays are 20-45 age employees as the map shows the peak of trips at work arrival and departure hours, while during the weekends the same 20-45 age people with the peak between 11 am to 6 pm. For user type variable, there is a clear difference in duration distribution between customers and subscribers where customers interquartile range of duration is higher than those of subscribers.


## Key Insights for Presentation

> For the presentation, I just focused on the the most important variables affecting the trip duration and no. of trips, so I started with the trips distribution and how the trips was categorized into three categories according to trip duration, then a clustered bar chart was used to show the importance of moderate and long trips as short trips, then a histogram was used to show how the trips distribution differs dependeng on whether the day is weekday or weekend, then the heat map was used to define the target segment age and time, ten finally the top 10 stations in each city was determined according to the total no. of trips where the trips were sub-divided into the three categories in each station.

## References

https://stackoverflow.com/questions/19412462/getting-distance-between-two-points-based-on-latitude-longitude
https://stackoverflow.com/questions/34279378/python-pandas-apply-function-with-two-arguments-to-columns
https://stackoverflow.com/questions/25146121/extracting-just-month-and-year-separately-from-pandas-datetime-column
https://stackoverflow.com/questions/32278728/convert-dataframe-date-row-to-a-weekend-not-weekend-value
https://matplotlib.org/3.3.3/gallery/lines_bars_and_markers/bar_stacked.html
https://www.geeksforgeeks.org/how-to-annotate-bars-in-grouped-barplot-in-python/
https://stackoverflow.com/questions/59466109/how-to-get-x-axis-labels-in-multiple-line-in-matplotlib

