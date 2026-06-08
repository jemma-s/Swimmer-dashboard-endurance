# Power BI Dashboard - Endurance results

This dashboard was designed for the Somerset Masters Swimming club for the endurance (E1000) competition. This competition runs annually and requires swimmers to complete a variety of 400m, 800m, 1500m 30MIN, 45MIN and 60MIN swims in different strokes across the year. 

Link: https://www.somersetmasters.org.au/copy-of-current-endurance-results 

![Demo](/screenshots/Demo-2026-06-08.gif)



## Purpose
To provide a monthly update to the Somerset Masters Swimming Club members of the E1000 scores on a club and member level. 

The key goals were as follows:
* Show a monthly snapshot of the current Somerset leaderboard. 
* As the E1000 website is not user friendly (https://e1000.msarc.org.au/results/results.php), provide an easier way to view completed swims and total points.
* Provide more in-depth analysis in time improvements and other statistics which are not directly shown on the E1000 website. 

A key consideration was to ensure graphs are easy to use and interpret. As Somerset Masters has members from a variety of backgrounds and ages, ranging from 19 to 90, clear graphs are essential in ensuring the accessibility of the dashboard is preserved. 

## Data source
Data has been scraped from the E1000 website using the Somerset recorder app (link TBA, Github folder is currently private). 

All data used is publicly accessible.  

## Dashboard views
### Club view
![Club view](/screenshots/club_view.png)

Features:
* Gives an overview of the club's key statistics, including total points, number of swims, number of swimmers, percentage of swims that achieved maximum points and average number of points per swimmer.
* Gives an overview of points per month over the year.
* Shows an overview of points per stroke and event.
* Shows the current leaderboard, conditionally coloured based on gender.
* Shows the swimmer who has achieved the greatest PB in a single event.
* Dynamically updates the date dependent on the most recent result in the dataset. 
  
### Swimmer view
![Swimmer view](/screenshots/swimmer_view.png)

Features:
* Allows for filtering by club member.
* Gives an overview of the swimmer's key statistics, including total points, number of swims, percentage of swims that achieved maximum points and current placings. 
* Gives an overview of points per day over the year.
* Displays an overview of points per stroke and event. 
* Gives insight into improvements that have been made over the year. Displayed in a table and a graph due to accessibility reasons.
* Dynamically updates the improvement table and graph to display "No improvement data found" when applicable.
* Dynamically updates placing text to be gold, silver and bronze coloured when the swimmer has placed 1st, 2nd or 3rd respectively.

### Improvement view
In a given event, a swimmer can either gain maximum, medium or minimum points based on how fast or far they swam. This is dependent on the swimmer's age group and gender: https://e1000.msarc.org.au/scoring/index.php 
![Improvement view](/screenshots/improvement_view.png)
![Improvement view - with table](/screenshots/improvement_view_table.png)

Features:
* Dives deeper to break down the selected swimmers' scores. 
* Visually shows the number of swims that have received certain score brackets based on distance.
* When applicable, displays a table that shows the date of a specific result and the improvement needed to reach the next point category.
* This page makes it easy for swimmers to identify which swims they need to improve on to receive more points.


## Future improvements
* The addition of previous E1000 data to compare performances over the years on a club and swimmer level.
    * This may require converting the data model to a snowflake model to easily allow for future year comparisons. 
   
