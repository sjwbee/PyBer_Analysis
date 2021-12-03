# PyBer Analysis

## Overview

The purpose of this project was to create a DataFrame of the ridesharing data categorized by city type (Urban, Suburban, and Rural). 
This DataFrame would then be visualized using Pandas and Matplotlib.

This project was accomplished using the city_data.csv and the ride_data.csv which were merged to create the pyber DataFrame: pyber_data_df

## Results

### Creating the Summary DataFrame

The summary DataFrame consists of 5 columns: Total Rides, Total Drivers, Total Fare, Average Fare per Ride, Average Fare per Driver. 
The index of this DataFrame is the type of city (urban, suburban, rural).

  -Total Rides: Calculated by using the groupby function with an argument of "Type" and the count function (counting ride_id) to determine how many rides occurred      within each type of city. 

  -Total Drivers: Calculated using the groupby function with an argument of "Type" and the sum function (adding driver_count) to determine the number of drivers in    each city. 

  -Total Fare: Calculated using the groupby function with an argument of "Type" and summing the amount of fare in each city type. 

  -Average Fare per Ride: Calculated by dividing the Total Fare by the Total Rides

  -Average Fare per Driver: Calculated by dividing Total Fare by Total Drivers

DataFrame was compiled by the folling code: 

<img width="1106" alt="Screen Shot 2021-12-02 at 5 18 31 PM" src="https://user-images.githubusercontent.com/90734050/144528492-9bfe7427-575d-44dc-896d-f58d11fa20e4.png">


### Creating a Line Chart of Results

Steps: 
1. Create a new DataFrame with the date and city type as indicies and the sum of fare for each date and city type as a value:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 19 16 PM" src="https://user-images.githubusercontent.com/90734050/144528540-2920941a-84af-466b-ac48-8b63ac8ee6ce.png">


2. Reset the index to use the pivot function:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 19 27 PM" src="https://user-images.githubusercontent.com/90734050/144528559-8562d98a-567f-4c05-ab52-7a04be23e94f.png">


3. Use the pivot function to make "date" the index, city types the columns, and fare totals the values:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 19 36 PM" src="https://user-images.githubusercontent.com/90734050/144528592-0f5b5d60-1bbb-4bcb-8d60-236a2153dea0.png">


4. Use the "loc" function to specify a specific timeframe to focus on:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 19 50 PM" src="https://user-images.githubusercontent.com/90734050/144528639-d81f2223-7ade-4cda-b511-9786fe01b9b3.png">


5. Change "Date" index to the datetime datatype:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 20 04 PM" src="https://user-images.githubusercontent.com/90734050/144528654-ce2c68ac-732a-438d-8cdd-3a3b1968ff99.png">


6. Create dataframe using the resample() function using "W" as an argument to get the sum of fare by each week:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 20 15 PM" src="https://user-images.githubusercontent.com/90734050/144528677-964c13eb-2b30-4e76-b0da-d35a8fb0fed9.png">


7. Create the plot:

<img width="1106" alt="Screen Shot 2021-12-02 at 5 20 36 PM" src="https://user-images.githubusercontent.com/90734050/144528702-66a140a6-0cdc-4a92-84a2-dc46933ec713.png">


###Description of Results

The Urban city type had the largest number of rides, drivers, and total fare, while the average fare per ride and per driver were higher in rural city types. 
This is likely due to the higher demand for rides in cities where a larger number of people are less likely to own personal vehicles. 
Because there are more drivers in these areas, there is more competition, thus lowering the price of the average ride, whereas there is less competition in rural areas, thus raising the price per ride and driver. 



## Summary

These results show that urban city types produce the greatest amount of profit for PyBer followed by Suburban and then Rural. 
Three recommendations I would make to the CEOs of PyBer is 1) to continue investing in Urban rideshare programs, especially in underserved areas that could benefit from greater mobility, 2) promote the use of clean, energy efficient vehicles that will enhance their image in urban spaces with a focus on environmental sustainability, 3) Look into developing more efficient urban spaces that will increase the number of urban dwellers, thus increasing the number of customers that will use the PyBer app. 
