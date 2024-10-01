# capstone-cyclistic-project
This is my first respository
I am an Engineer and have done MBA also.I have basic knowledge of C,Python and R Programming.
Author - Mayank Vatsa


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


