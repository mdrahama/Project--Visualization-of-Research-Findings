# Ford GoBike System Dataset Exploration
## by Md Rahamat Ullah...........................


## Dataset

> The data consists of information regarding bike hiring of FordGo Bike from 2017 to February 2020. The dataset can be found in Ford GoBike website (https://www.lyft.com/bikes/bay-wheels/system-data).

The data consisted of 15 different variables such as :
bike_id                    
bike_share_for_all_trip    
duration_sec               
end_station_id             
end_station_latitude       
end_station_longitude      
end_station_name           
end_time                   
rental_access_method       
start_station_id           
start_station_latitude     
start_station_longitude    
start_station_name         
start_time                 
user_type                  

  Each dataset was monthly basis. Dataset was in zip format. I have done following wrangling steps to make my data ready for analysis.
- Folder creation in local drive to save data
- Simple crawling to save the URLS of the zip files of the dataset from website 
- Downloading the zip files and extracting csv files from zip files
- Reading and concating all csv files on 4/18/2020 12:05 EST, in "Merged File" folder. Name of the merged file is 'final.csv'
- Dealing with missing values in 'start_station_id', 'start_station_name', 'end_station_id', 'end_station_name'
- After cleaning the major issues, when the file was ready for analysis, it was saved as 'Cleaned.csv' inside 'Merged File' so all the analysis in the future can be done without repeating above steps.



## Summary of Findings:

- Duration(minutes) has a slightly long-tailed distribution, with a lot of trips on the low duration end, and few on the high duration end. When plotted on a log-scale, the price distribution looks unimodal, with one peak at 10 minutes.
- Most of the users are subscriber. 
- Most of the users rented the bike through app.
- Most of the users didn't share the bike throughout the trip.
- FordGo Bike rental is increasing each year.
- Bike rental is the heighest on October, September and August repectively. Bike usage is the lowest on December, May and April repectively.
- Number of trips are low on weekend and high on weekdays.
- Bike usage is fairly consistance over dates of months. Ignoring usage on 31 as not all months include 31st day.
- Most of the people rent the bike at 5pm, 8am, 6pm and 9am respectively. 
- Most of the users of app are subscriber. Also, Most of the users of clipper are subscriber
- Only subscribers shared bike for all trip. 
- Median Duration(minutes) is fairly consistent over months. Median is around 10 minutes. 25 percentile is above 5 minutes. 75 percentile is around 14 minutes. From, the boxplot it doesn't look like duration of trips varies that much based on months.
- Duration of trips vs Hours of day, boxplot shows that there is a trend between duration of trips and clock hours. Median of duration(min) is highest for 1pm and 11pm rental and lowest for 7 am & 12 am rental. In general median is around 10 minutes and 75 percentile is between 10 minutes and 20 minutes.
- Duration of trips vs Day, boxplot shows that there is a trend between duration of trips and Day. Median and 75 percentile of duration(min) is highest for weekend compared to weekdays. 
- The largest mean duration of trips are found in Wednesday at 3am, Sunday at 8 pm, Saturday at 7 pm, Thursday at 1 am, Monday at 11 pm


## Key Insights for Presentation:

> Most interesting features from the exploration findings that should be visualized in the presentation are the distribution of user type, distribution of Duration, type of most of the users,  rental access method, monthly/weekly/hourly trend of FordGo Bike rental. This will give an initial idea about what type of users use the FordGo Bike, how do they use it, when do they use it. So we will get a mental picture of the frequency of Trips. Next, Duration vs month, Duration vs clock hour and Duration vs day of week will give us an idea of how duration is dependent on those factors. Lastly, a visual representation of mean duration vs clock hour and day of week can help to understand the time-day when FordGo Bike company can expect to have longer use of their bike. 