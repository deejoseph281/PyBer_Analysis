# PyBer_Analysis

## Overview of the Analysis
### Purpose
The purpose of the new analysis was to understand the data for Pyber rides for each city type, which included Total Rides, Total Drivers, Total Fares, Average Fare per Ride, and Average Fare per Driver for Rural, Urban, and Suburban cities. The analysis will help the CEO V. Isualize make decisions about which types of cities need more driver support and which city types are generating the most money.

## Results
 Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types.
### Getting a Summary Data Frame
We had two data sets regarding city_data and ride_data that needed to be merged into a single dataset for the purpose of the analysis. 

![image](https://user-images.githubusercontent.com/115019829/200454933-3a88390b-e7aa-435e-9da7-9fe0234a1ed6.png)

### We then needed to use the .count() function to count ride_id and rider_count by "type" and get the total fare by using the .sum() function to calculate the total fare by "type". Lastly, we needed to calculate the average fare per ride and average fare per driver by utilizing .groupby() outputs to calculate the total fares / total rides and total fares / total drivers per "type". 

![image](https://user-images.githubusercontent.com/115019829/200455387-d487a68e-6526-422b-beb7-d8ef24a6ab2e.png)

With the information, we were able to summarize the data into a single data frame to consolidate our required analysis datapoints. 

![image](https://user-images.githubusercontent.com/115019829/200456604-cbf450a7-0125-4aad-ade7-ad8f4599e7d1.png)


### Differences in Ride Sharing Among the Different City Types
![image](https://user-images.githubusercontent.com/115019829/200454814-3916c4dc-3d3f-4d70-9d1e-79037a0bf22f.png)


## Summary
Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types.
