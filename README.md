### Google Data Analytics Capstone - Cyclistic Data
<br>
Cyclistic is a bike-share program that has a fleet of 5824 that are geotracked and locked into a network of 692 stations across Chicago. There are two primary types of customers: casual riders and annual members. The director of marketing believes that the company's future success depends on maximising the number of annual memberships. Hence, as a junior data analyst at the company, I have been tasked with answering the following question - "How do annual members and casual riders use their Cyclistic bikes differently?" The case study follows an analytical roadmap that consists of these phases: Ask, Prepare, Process, Analyze, Share, Act. 

<br>

### ASK
<br>
First, I defined the business question that my analysis intends to answer : "How do annual members and casual riders use Cyclistic bikes differently?". The key stakeholders in this project are the Director of Marketing, the marketing analytics team and the executive team. 

<br>

### PREPARE & PROCESS
<br>
I have chosen to use Python as my analytical tool to clean, process, analyze and visualize the dataset. I imported the most recent 12 months of Cyclistic bike data to clean and process it initially. Upon examination of the dataset, there are 13 variables, namely: Ride ID, Rideable Type (type of bike), Start Time (ride), End Time (Ride), Start Station ID, Start Station name, End Station name, End Station ID, Latitude and Longitude of Start and End stations,   After checking for null values in the data, I computed the percentage of null values. A rule of thumb is that up to 10 percent of null values in a dataset can be dropped, so as to not affect the sample size negatively. Since this condition was satisfied, I dropped the null values to clean the dataset. 
<br>
Trip duration was also calculated for each ride, and the results were sorted into a new variable "Trip Dutation". This variable is a key variable of interest. However, I discovered that the trip duration for some of the rides was less than 0 or 0. This could be interpreted as wrongly entered data, or rides that were cancelled upon booking. It then made sense to drop the trips with duration <=0, so I did. 

<br>

### ANALYZE
<br>
It was found that the number of annual members is higher than the number of casual riders. It was also found that the average trip duration is much higher for a casual rider than an annual member. This makes sense as one can assume that casual riders would want to get maximum value out of their single trip or full day passes by riding for as long as possible, as opposed to annual members who would be indifferent to a single ride's monetary value. One important thing to note here, is that I chose to use median instead of mean as the aggregator to determine the "average". This is due to the fact that around 4000 records in the dataset contain trip durations of more than 1000 minutes. These outliers affect the mean trip duration. Hence, median trip duration is a better representative of riding patterns. 

<br>

Another insight that I gathered is that the number of trips are the highest on Saturday, followed by Sunday and then Friday, meaning that ride traffic is highest on the weekends. Moreover, the median trip duration for annual members is much lower than the median trip duration for casual riders. This could tie into the earlier assumption, that casual riders could be looking to extract maximum value out of singular rides. 

<br>

The type of bike being used the most by casual riders and members is the docked bike, followed by the classic bike and then the electric bike. The next step in my analysis was to create a month variable to analyze season-based trends in ridership. For both casual riders and members, the months of June, July and August showed the highest riderships, which again makes sense as these are the summer months in Chicago. The last step was to analyse the median trip duartion for casual riders and casual riders had the highest median trip durations, in the summer months as well as the rest of the year, as opposed to annual members. 
<br>

### SHARE
<br>
I used Matplotlib, the data visualization package in Python, to make the following visualizations: Frequency of Trips by the Day of the Week, Median Trip Duration by User Type and Day of Week, Number of Trips by User Type per month, and Median Trip Duration by User Type per month. 

<br>

### ACT
Here are some key insights derived from my analysis, with reference to the primary business question: "How do annual members and casual riders use Cyclistic bikes differently?"
<br>

1) Average trip duration is much higher for a casual rider than an annual member, throughout the year. 
2) Frequency of trips is highest on Sunday, Saturday and Friday respectively, for both casual riders and annual members. 
3) The type of bike being used the most by casual members and annual members is the docked bike.
4) The summer months of June, July and August have the highest ridership for casual riders and annual members.
