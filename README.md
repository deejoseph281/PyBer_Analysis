# PyBer_Analysis

## Overview of the Analysis
### Purpose
The purpose of the new analysis was to understand the data for Pyber rides for each city type, which included Total Rides, Total Drivers, Total Fares, Average Fare per Ride, and Average Fare per Driver for Rural, Urban, and Suburban cities. The analysis will help the CEO V. Isualize make decisions about which types of cities need more driver support and which city types are generating the most money.

### Analysis
 Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types.
### Getting a Summary Data Frame
We had two data sets regarding city_data and ride_data that needed to be merged into a single dataset for the purpose of the analysis. 

![image](https://user-images.githubusercontent.com/115019829/200454933-3a88390b-e7aa-435e-9da7-9fe0234a1ed6.png)

We then needed to use the .count() function to count ride_id and rider_count by "type" and get the total fare by using the .sum() function to calculate the total fare by "type". Lastly, we needed to calculate the average fare per ride and average fare per driver by utilizing .groupby() outputs to calculate the total fares / total rides and total fares / total drivers per "type". 

![image](https://user-images.githubusercontent.com/115019829/200455387-d487a68e-6526-422b-beb7-d8ef24a6ab2e.png)

With the information, we were able to summarize the data into a single data frame to consolidate our required analysis datapoints. 

![image](https://user-images.githubusercontent.com/115019829/200456604-cbf450a7-0125-4aad-ade7-ad8f4599e7d1.png)

### Creating a Pivot Table DataFrame for January 2019 to April 2019

We needed to create a pivot table to get the sum of the dares for each date to begin further analyzing the months that were requested by Pyber. 

We begin the pivot table process through the groupby() function and grouping the date, type, and using .sum() by fare to show the indices  required for the output. We ensured that we reset the index on the DataFrame, which is required to use the pivot() function in Python.

![image](https://user-images.githubusercontent.com/115019829/200457217-68b24bc8-d593-45cd-b84c-a2aaa43b79e7.png)

We then created the pivot table using the date as the index, type for the columns, and fare for the values for each date. We then ensure we used .loc to deep dive into January - April 2019 specifically. 

![image](https://user-images.githubusercontent.com/115019829/200457491-99abbe74-9537-4d09-afc7-c9469eb7808f.png)

At this point, we noted that the date index in our pivot was not set to datetime, so we converted it from a float data type to datetime data type. 

![image](https://user-images.githubusercontent.com/115019829/200457648-22688819-1528-4bd4-bd7c-619515b24265.png)

Finally, we consolidated the dates from individual dates to weekly summary of each month so we could easily view the data in a line-chart and identify trends within each month, if applicable. 

![image](https://user-images.githubusercontent.com/115019829/200457813-14c8865b-8d10-4b20-af9b-bac11fcbc8bd.png)

### Results

#### Differences in Ride Sharing Among the Different City Types

The difference in ride sharing among the different city types are: 
* Urban rides have higher demand than both rural and suburban rides. 
* Drivers in rural and suburban cities are making more trips, and therefore, earning more average fares per driver. 
* 32% of drivers in urban cities are not actively making trips. 

## Summary
Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types.

### Recommendations to Pyber 
* Urban cities make the most money based on volume alone, and therefore, we should expand the dates to see if there are specific months or seasons where we see more drivers participating in Pyber. 
* Rural cities make the most per trip, we would recommend reviewing deeper into which rural cities are utilizing Pyber more, and which rural cities are using Pyber less or not at all. 
* We recommend reviewing the strongest and weakest cities in Pyber based on the number of drivers and trips per city to understand if there are specific regions that are underserved by drivers. 

