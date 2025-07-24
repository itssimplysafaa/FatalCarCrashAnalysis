# Fatal Car Crash Analysis Power BI Dashboard

### Purpose
The purpose of this dashboard is to provide a high-level overview of Fatal Car Crash Data in the city of Charlotte, North Carolina
from the years 2019 to 2023.

### Important Questions
What days of the week and times of day are the most fatal car crashes happening? 

What types of fatal car crashes are the most common? 

What are the most common causes of fatal car crashes?

What areas of Charlotte are the most fatal car crashes happening?


### Data Sources and Tools
The dataset is public through the City of Charlotte's website.
https://data.charlottenc.gov/datasets/charlotte::fatal-or-serious-injury-crashes/explore

For locational data, I used Google Maps API for reverse geocoding.

### Data Transformation 
I removed columns that wouldn't add to the analysis, such as the crash type number and primary description numbers. Many of the data entries had primary descriptions such as "no contributing circumstance", or "unable to determine". Therefore, I grouped all of those descriptions under the category, "Unknown". "The military time column's format was a whole number, so I converted the column into standard time using DAX and made it into a separate column. I then made a separate column for hour intervals (i.e., *7:00 AM*), to group the fatal crashes more efficiently. I added a location column, zipcode column, and neighborhood column, using DAX, Power Query and Google Maps API to give more context to the latitude and longitude coordinates.


### Visuals In Dashboard
**Fatal Crashes by Year and Month** -
A drill-down clustered column chart showing the total number of fatal crashes by month and year. There is also a month and year slicer that
can be used to choose a specific month of a specific year (i.e. February 2023).

**Fatal Crashes by Day of Week and Time** -
A drill-down clustered column chart showing the total number of fatal crashes by day of the week and time. 

**Leading Causes of Fatal Crashes** -
A clustered bar chart, showing the leading causes of fatal crashes and corresponding numbers.

**Most Common Fatal Crash Types** -
A clustered bar chart, showing the most common types of car crashes and corresponding numbers.

**Fatal Crashes by Zipcode** -
A bubble map showing the number of fatal crashes by Zipcode and Neighborhood. To get addresses from latitude and longitude 
coordinates I reverse-geocoded the coordinates using Google Maps API and power query and extracted the zip codes into a separate
column. For neighborhoods, I assigned each zipcode to a neighborhood using DAX.

**Top 10 Zip Codes** -
A table that shows the 10 zip codes in Charlotte with the most fatal crashes in descending order.

**Top 5 Neighborhoods** -
A clustered column chart showing the 5 neighborhoods in Charlotte with the most fatal crashes in the last 5 years.

### Conclusions Drawn
- 2021 had the most fatal crashes in the 5 years with 185 fatal crashes. 
- Weekends are when the most car crashes happen with Saturday having the highest number overall at 144. Sunday comes in second with 128 crashes overall in the last 5 years.
- Fatal car crashes tend to happen at night with the most common time for them to happen being between 8 and 10 PM.
- Pedestrian crashes make up over a quarter of fatal car crashes over the 5 years.
- After 2019, speeding became the number 1 cause of fatal car crashes.
- The Zipcode with the highest number of fatal crashes overall is 28208 which is where the Wesley Heights Neighborhood and Charlotte Douglass International Airport are located
- University City, including the University of North Carolina at Charlotte and surrounding areas, had the highest number of fatal crashes in the last 5 years at 116 fatal crashes.
 

