# Fatal Car Crash Analysis Power BI Dashboard

### Purpose
The purpose of this dashboard is to provide a high-level overview of Fatal Car Crash Data in the city of Charlotte, North Carolina
from the years 2019 to 2023.

### Data Sources and Tools
The dataset is public through the City of Charlotte's website.
https://data.charlottenc.gov/datasets/charlotte::fatal-or-serious-injury-crashes/explore

For locational data, I used Google Maps API for reverse geocoding.

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

**Top 10 Zip Codes**
A table that shows the 10 zip codes in Charlotte with the most fatal crashes in descending order.

**
