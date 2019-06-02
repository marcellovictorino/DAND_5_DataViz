# Ford Go Bike - 2017 - 2019
## by Marcello Victorino

## Dataset

The Ford Go Bike is the Bike-share system operating in the Bay Area, San Francisco (USA). With around 6.400 bikes in more than 360 stations across San Francisco, East Bay and San Jose, there are basically two types of subscription:

1. Subscriber: Membership can be Monthly ($15/mo) or Annual ($150/yr, equivalent to $12.50/mo). It grants unlimited 45-minutes trips
2. Customer: 
   + Single ride ($2 per trip) and 
   + Access Pass ($10), granting unlimited 30-minute rides within 24 hours.

The [dataset](<https://www.fordgobike.com/system-data>) is open to the public, containing station and user data for each trip. At the time of this project, is was possible to download historic data from January, 2017 up to April, 2019.

The raw data was spread out into 17 files. After appending all into a single data frame, I performed some Data Wrangling, summarized in the following:
### Data Wrangling
+ **Missing values**: there were around 220 thousand observations missing data for user gender and birth year. Instead of applying imputation techniques (median and mode for numerical and categorical variables, respectively), I decided to drop these rows.
+ **Bike Share For All Trip**: this variable is not present in the 2017 data. I filled all 2017 missing data as 'No', since the special pricing program for qualifying low-income users in the Bay area wasn't in place at the time.
+ **Station Data:** to improve performance, I created a new table holding unique values for the station ID and their name, removing the Start and End station name from the main dataset. It is possible to retrieve this information afterward by merging the data on the unique station ID.
+ **Data Type**: 
  + 'station_id' stored as string instead of float
  + 'member birth year' stored as integer instead of float
  + end and start time stored as date-time

### Feature Engineering

After dealing with data integrity issues, I transformed some variables into a more meaningful format and extracted the components of the start time variable:

+ Transformed member gender into binary variable, where 1: Male, 0: Female.
+ Transformed User Type into binary, where 1:Subscriber (Annual Pass), 0: Customer (Single Ride or Access Pass)
+ Transformed Low Income Trip into binary, where 1: Yes, 0: No.
+ Transformed trip duration from seconds to minutes.
+ Calculated user age at time of bike rental.
+ Extracted from Start Time of rental: year, month, week, day, day of week, and hour

After this process, the final dataset has over 3 million observations with 19 columns, containing information over the initial and final bike station, time of start of the trip, duration in minutes; as well as details over the user, such as gender, age, and member status (subscriber or not).




## Summary of Findings

> Summarize all of your findings from your exploration here, whether you plan on bringing them into your explanatory presentation or not.


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.