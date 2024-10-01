# capstone-cyclistic-project
This is my first respository
I am an Engineer and have done MBA also.I have basic knowledge of C,Python and R Programming.
Author - Mayank Vatsa

I used Cyclistic’s historical trip data to analyze and identify trends by downloaded  the previous 12 months(September 2023 to August 2024) of Cyclistic trip data [here](https://divvy-tripdata.s3.amazonaws.com/index.html). (Note: The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study, the datasets are appropriate and will enable you to answer the business questions. The data has been made available by Motivate International Inc. under this license.) This is public data that you can use to explore how different customer types are using Cyclistic bikes. But note that data-privacy issuesprohibit you from using riders’ personally identifiable information. This means that you won’t beable to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes.



I analyzed a dataset using R for a company, Cyclistic, a bike sharing company in Chicago. Created an interactive dashboard showing how annual members and casual riders use Cyclistic bikes differently. I also provided marketing strategies to convert casual riders to annual members.


Cyclistic is a fictional bike sharing program which features more than 5,800 bikes and 600 docking stations. It offers reclining bikes, hand tricycles, and cargo bikes, making it more inclusive to people with disabilities and riders who can't use a standard two-wheeled bike. It was founded in 2016 and has grown tremendously into a fleet of bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.
Previously, Cyclistic's marketing strategy tried to build the general awareness and appeal to broad consumers. It has flexible pricing plans: single-ride passes, full-day passes, and annual memberships. Those who purchase single-ride or full-day passes are referred to as casual riders while those who purchase annual memberships are Cyclistic members. 

My Role: In this scenario I am a junior data analyst at Cyclistic and my team has been tasked with the overall goal (see below) of designing marketing strategies 


Overall Goal: Design marketing strategies aimed at converting casual riders into annual members.


Business Question: "How do annual members and casual riders use Cyclistic bikes differently?"


Below I will describe step-by-step the process I used to for this project. 



#PROCESS:
Overview: I first analyzed the data separately (each month) in Excel, then used R to analyze the data as a whole (one year). Finally I created a dashboard in Tableau and used Figma to support the design elements. 


#Microsoft Excel
I initially wanted to gather and analyze my data in Excel because it was the tool I was most familiar with and I could get a general understanding of the data quicker. I did not combine all of the spreadsheets into one because that would've taken more processing power than my computer had. 

I began downloading the data from divvy-tripdata, and turning the .csv files into excel spreadsheets. I downloaded the most recent year of data which was at the time of starting my project: 

September 2023

October 2023

November 2023

December 2023

January 2024

February 2024

March 2024

April 2024

May 2024

June 2024

July 2024

August 2024

Added two columns to all of the months:

ride_length calculated the total ride length for each trip using the start_at column which was: ending time minus starting time. 

day_of_week calculated the day of the week for each trip using the start_at column date. 

Went over the business task and the information I had at hand and how that could be used to figure out how members and casual riders use the bike service differently

Came up with metrics to look at such as : 

total number of rides per hour, per day of the month, per season, per day of the week, and for different bike types 

Average ride length between members and casual

For every month in Excel created pivot tables and charts to go with the analysis on (this took the longest):

Total Rides per Weekday - calculated the total rides for members and casual and separated it by day of the week; used a cluster column chart

Average Ride Length - calculated the average ride length for members and casual and separated it by day of the week; used a cluster column chart

Total Rides per Hour -  calculated the total rides for members and casual separated by the time of the day (24hr); used a line comparison chart 

Total Rides per Day -  calculated the total rides for members and casual separated by the day of the month; used a line comparison chart 

Total Rides per Bike Type - calculated the total rides for members and casual separated by Bike type; used stacked column chart 

#R 
I originally wanted to use SQL but the files were too big to upload and I couldn't figure out how to utilize Google Cloud Platform. Instead I used R to analyze the data because it could handle all of the information quicker than Excel, and I wanted to work on my R skills. Below is my general process in R, I didn't include my mistakes/missteps or errors for the sake of brevity.


View my full code on my Github for this capstone project here. 

Load all of the libraries I used: tidyverse, lubridate, hms, data.table 

Uploaded all of the original data from the data source divytrip into R using read_csv function to upload all individual csv files and save them in separate data frames. For august 2020 data I saved it into aug08_df, september 2020 to sep09_df and so on. 

Merged the 12 months of data together using rbind to create a one year view

Created a new data frame called cyclistic_date that would contain all of my new columns 

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

Cleaned the data by:

Removing duplicate rows

Remove rows with NA values (blank rows)

Remove where ride_length is 0 or negative (ride_length should be a positive number)

Remove unnecessary columns: ride_id, start_station_id, end_station_id, start_lat, start_long, end_lat, end_lng

Calculated Total Rides for:

Total number of rides which was just the row count = 4,152,139

Member type - casual riders vs. annual members 

Type of Bike - classic vs docked vs electric; separated by member type and total rides for each bike type

Hour - separated by member type and total rides for each hour in a day

Time of Day - separated by member type and total rides for each time of day (morning, afternoon, evening, night)

Day of the Week - separated by member type and total rides for each day of the week

Day of the Month - separated by member type and total rides for each day of the month

Month - separated by member type and total rides for each month

Season - separated by member type and total rides for each season (spring,  summer, fall, winter)

Calculated Average Ride Length for:

Total average ride length

Member type - casual riders vs. annual members 

Type of Bike - separated by member type and average ride length for each bike type

Hour - separated by member type and average ride length for each hour in a day

Time of Day - separated by member type and average ride length for each time of day (morning, afternoon, evening, night)

Day of the Week - separated by member type and average ride length for each day of the week

Day of the Month - separated by member type and average ride length for each day of the month

Month - separated by member type and average ride length for each month

Season - separated by member type and average ride lengths for each season (spring,  summer, fall, winter)

#Tableau 
While I learned the basics of Tableau in the Google Course I wanted more practice with visualizing data



![image](https://github.com/user-attachments/assets/3c87c69a-c62e-40ee-8c03-ce29e3ce0b45)





# Creating Dashboard

With the help of Microsoft Excel and Tableau I created a Dashboard whose details are attached as Dashboard details

 

