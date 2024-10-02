# capstone-cyclistic-project

Author - Mayank Vatsa

This is my first respository.

I am an Engineer and have done MBA also.I have basic knowledge of Python and R Programming.



I used Cyclistic’s historical trip data to analyze and identify trends by downloading the previous 12 months(September 2023 to August 2024) of Cyclistic trip data [here](https://divvy-tripdata.s3.amazonaws.com/index.html).  This is public data that can be used to explore how different customer types are using Cyclistic bikes. 

## Brief introduction of the company

Cyclistic is a fictional bike sharing program which features more than 5,800 bikes and 600 docking stations. It offers reclining bikes, hand tricycles, and cargo bikes, making it more inclusive to people with disabilities and riders who can't use a standard two-wheeled bike. It was founded in 2016 and has grown tremendously into a fleet of bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.
Previously, Cyclistic's marketing strategy tried to build the general awareness and appeal to broad consumers. It has flexible pricing plans: single-ride passes, full-day passes, and annual memberships. Those who purchase single-ride or full-day passes are referred to as casual riders while those who purchase annual memberships are Cyclistic members. 

## My Role: 
In this scenario I am a junior data analyst at Cyclistic and my team has been tasked with the overall goal of designing marketing strategies 


## Overall Goal:
Design marketing strategies aimed at converting casual riders into annual members. That is the data analysis in this project shuold be confined to [conversion of casual members to members]


## Business Question:
1. Based on data such as numbers of riders, preffered bike type, preffered season, ride length, etc. how do members and casual riders use Cyclistic bikes? 
2. Secondly what steps the compnay should take to convert the casual riders to annual members?


Below is step by step description of the process I did for this project. 

## PROCESS:
[Overview]:
I first analyzed the data separately (each month) in Excel, then used R to analyze the data as a whole (one year). Finally I created a dashboard to support design elements.

I initially wanted to gather and analyze my data in [Excel] because it was the tool I was most familiar with and I could get a general understanding of the data quicker. But due to limitaions in excel spreadsheet, combining the 12 moths data(which sums about 5 million) was not possible. As such I went for [R Studio] where using [rbind] function the data of all 12 files were combined.
However besides RStudio and Tableau, Excel was used for generating pivot table and other charts for analysis.

## STEPS TAKEN:
1. I downloaded 12 months data from [divvy-tripdata](https://www.google.com) , and converted the .csv files into excel spreadsheets. However data in both csv and excel were kept for analysis purpose. The data was downloded from September 2023 to August 2024. 

2. Added two columns namely ride_length and day_of_week to all of the months:

ride_length:

Calculated the total ride length for each trip subtracting end_at and  start_at column.

day_of_week:

Calculated the day of the week for each trip using [weekday] function in start_at column. 

3. For every month in Excel created pivot tables and charts to go with the analysis.

## Using R for processing of data

I tried to use SQL and Bigquery for preparing data for analysis, but I was comfortable with R programming, because during my learning at Coursera , the wonderful teachers made concepts easy to understand and further the online assignments helped  me to grasp the concept of R programming. I found R very user-friendly and easy to understand.

Below is my general process in R. My full code can be viewed in my [Github profile].

Libraries used in R: tidyverse, lubridate, hms, data.table 

Uploaded all of the original data from the data source [divytrip](https://www.google.com)  into R using read_csv function to upload all individual csv files and save them in separate data frames. 

Merged the 12 months of data together using  [rbind] to create a one year view.

Created new columns for:

Ride Length - did this by subtracting end_at time from start_at time

Day of the Week 

Month 

Day 

Year

Time - convert the time to HH:MM:SS format

Hour 

Season - Spring, Summer, Winter or Fall

Time of Day - Night, Morning, Afternoon or Evening

Created a new data frame called [cyclistic_date] that would contain all created new columns 

## Cleaning of data:
Removed duplicate rows, rows with NA values (blank rows),
removed columns where ride_length was 0 or negative (ride_length cannot be negative),
removed unnecessary columns  namely ride_id, start_station_id, end_station_id, start_lat, start_long, end_lat, end_lng.

Calculated total ride_length  for:

Total number of riders

Total number of casual riders and member riders

Types of Bike used classic vs docked vs electric used in riding.


Time of Day - separated by member type and total rides for each session of day (morning, afternoon, evening, night)

Day of the Week - separated by member type and total rides for each day of the week

Day of the Month - separated by member type and total rides for each day of the month

Month - separated by member type and total rides for each month

Season - separated by member type and total rides for each season (spring,  summer, fall, winter)

Calculated Average Ride Length for:

Member and casual riders 

Type of Bike - used by riders and average ride length for each bike type

Hour - spent  by riders and average ride length for each hour in a day

Time of Day - spent by riders and average ride length for each time of day (morning, afternoon, evening, night)

Day of the Week - day-wise rides by all riders and average ride length for each day of the week

Day of the Month - ride length covered by both casual and member riders for each day of the month

Month - ride length for each month covered by both casual and member riders

Season - ride lengths for each season (spring,  summer, fall, winter) covered by both casual and member riders

Starting Station Names- Top 5 Starting Station Names with maximum number of casual riders.This was important for taking steps for converting maximum number of casual riders to member riders.

# Use of Tableau 
I learned the basics of Tableau after enrolling in Coursera for Google Certification Course. During the sessions of this course and with their awsome teaching skills, I became very confortable in Tableau and R. I used Tableau alongwith R for my final analysis of combined data on the basis of the charts made in Tableau. Its a wonderful tool for data analysis and interpretation

# Creating Dashboard

With the help of Microsoft Excel and Tableau I created a Dashboard whose details are attached as Dashboard details



 

