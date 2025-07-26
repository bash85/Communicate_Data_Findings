# Communicate_Data_Findings
This project has two parts that demonstrate the importance and value of data visualization techniques in the data analysis process.

In this project, the data exploration process followed the following steps:

1. Loading the dataset manually, then perform the following dataset cleaning and feature engineering steps:
  - Convert the data type for both the start_time and the end_time from object to datetime.
  - Create a new column in the dataframe called start_hour, through extracting the hour from a datetime.
  - Create a new column in the dataframe called start_day, through extracting the day name from a datetime. Then reorder the days of the week starting from 'Sunday' to 'Saturday', and convert it's data type into      Category.
  - Create a new column in the dataframe called duration_min, includes the trip duration in minutes. Values in this column were calculated by deviding values in the duration_min by 60.
  - Create a new column in the dataframe called member_age, includes the age of each member. Values in this column were calculated by substracting values in the member_birth_year from the current year of the data     collection, which was (2019).
  - Convert the data type of start_station_id, end_station_id, member_birth_year and member_age from float64 into Int32.
  - Reorder the new created columns to be next to the column extracted from.
  - Create a new cleaned dataframe called created_bike_df from the original dataframe bike_df, excluding all records with Null values in any column.
2. Started investigating the distribution of individual features using univariate visualizations. The used visualizations in this section were histograms for investigating the distribution of the trip duration in seconds and minutes, member_age and start_hour, besides having countplots for investigating the distribution of user_type and member_gender.
3. In the bivariate visualizations section, I investigated relationships between two variables, using boxplots to compare trip duration duration_min distributions between user types user_type, and to compare trip duration duration_min distributions between gender groups member_gender. Also, scatter plot was used to provide investigation of duration_min vs. member_age. Then I used a clustered bar chart to visualize the distribution of member_gender by user_type. A heatmap was used to visualize trip frequency patterns by start_hour and start_day.
4. The last section including multivariate analysis, the exploration of relationships between three or more variables were provided, so a facet grid with boxplot was used to show the age distribution by user type and gender. Then, used a scatter plot with multiple encodings to visualize the relationship between member_age and duration_min.

The following are the summary of the main findings from the data exploration:

- Most bike trips are short, but casual 'Customers' consistently take significantly longer trips than 'Subscribers'. Trip durations for 'Subscribers' tend to shorten during weekday commute hours, while 'Customers' trips can remain long even then.
- Trips are far more common on weekdays, especially Tuesdays through Thursdays, indicating a strong commuter base. Daily activity peaks during morning (8-9 AM) and evening (5-6 PM) commute hours, with minimal overnight use.
- 'Subscribers' make up most users and typically take short, functional trips, while the smaller group of 'Customers' take longer, more recreational trips.
- 'Male' users, particularly 'Subscribers', are the most numerous. The core user base is aged between 20s and 40s, while age doesn't strongly dictate trip duration, 'Subscribers' ages are more concentrated than 'Customers', who show a wider range.

The second part provides a presentation to explore the Ford GoBike system data and highlight the key insights into the bike-sharing system, through identifying who uses the service, when they use it and how they use it. This will provide data-driven insights that will help in improving the service efficiency and enhancing the user experience.
To obtain this, the main focus was on the trip duration (duration_min), user type (user_type), gender (member_gender), age (member_age) and trip start time (start_time).

## Dataset Overview and Executive Summary
The dataset consisted of 16 attributes for more than 183k bike trips in the Ford GoBike trip data from February 2019. The user age member_age was extracted from member_birth_date, and the duration_min was calculated from the duration_sec, also the start_hour and start_day were extracted from the start_time variable. After cleaning the data by removing inconsistencies and missing values, a new cleaned dataset consists of 19 attributes and almost 175k records for bike trips will be used in this part.

## The key findings were:

- Most trips were very short, but in general, casual 'Customers' have slightly longer trips than 'Subscribers'.
- The bike-sharing service is busiest during weekdays, especially from 'Monday' to 'Thursday' with morning and evening rush hours based on the commutes.
- The majority of trips were made by 'Subscribers' user type and 'Male' gender, where most of their trips were short and functional trips, and their age were usually between 20s and 40s.
