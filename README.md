# Ford-GoBike_Analysis

# About Dataset
The dataset has anonymous information about individual rides made in a bike-sharing system covering the greater San Francisco.
Start time and end time consist of only the mm:ss:SSS components of the timestamp element

### *Dataset Schema*
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/8c22eadb-0715-4b20-a707-20b5a9a558d6)

### *Dataset Snippet*
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/2a617e22-9742-409e-a157-fe0ac32c491c)



# Aim of Project
* Explore the usage of PySpark for big data analysis
* Identify patterns between bike usage and other parameters such as customer age and gender

# Methodology
Python programming language was used, employing several tools and libraries for the project.
### *IDE* 
* **Google Colab**
### *Libraries*
* **PySpark** - For general data exploration and analysis
* **Pandas** - Assiting in generating plots
* **Matplotlib** - For creating visualizations
* **Haversine** - For calculating the distance between 2 coordinates
* **Folium** - For generating map of station locations

# Results

## *General Insight into Dataset*
* *Total Number of Trips* - **519700**
* *Total Number of Stations* - **272**
* *Total Number of Bikes* - **3673**

### User Type Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/b0c1f178-eb07-442a-8050-bcb7bc70f943)

Bike users are categorized into 2 groups, ***customers*** who were responsible for ***110470*** trips representing ***21.26%*** of the total number of trips and ***subscribers*** who were responsible for ***409230*** trips representing ***78.74%*** of the total number of trips

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/7675adfc-bca0-4daa-bba8-97dff40ffeb0)

For user type, it was discovered that the average trip distance, average trip duration and average trip revenue are all directly proportional to each other, suggesting a strong positive correlation. Also, despite the number subscribers dwarfing the number of customers, it was realized that for all the parameters measured, customers did better averagely as compared to the subscribers which may suggest a negative correlation, whereby as the specific user type increases, the average trip distance, revenue and time decreases


### User Gender Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/abeaf08e-dd9f-41b6-8e08-f233a52218ee)

* ***Males*** were responsible for ***348,318*** trips representing ***67.02%*** of the total
* ***Females*** were responsible for ***98,621*** trips representing ***18.98%*** of the total
* ***Other*** were responsible for ***6,299*** trips representing ***1.21%*** of the total
* Bike users who did not specify their gender were categorized as ***Unspecified*** and were responsible for ***66,462*** trips representing ***12.79%*** of the total

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/6f9fb3e9-2b02-4249-adfd-ee44d6b560cd)
Similar to user type,  the average trip distance, average trip duration and average trip revenue are all directly proportional to each other for the specific genders. Also there seems to be a repeating trend where as the gender increases, the metrics measured decrease

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/e67a6999-1a42-4e1d-8dc3-0f37775d98f0)

The correlation heatmap confirms the hypothesis, indicating a ***perfect positive correlation*** among the usage duration, trip distance and trip revenue.
It was also realized that categorical data(***user type, member gender***) showed an internal negative correlative relationship. This indicates, as evident from the chart that, within the same category, there is a contrasting relationship with the metrics measured(***usage duration, trip distance and trip revenue***) except for ***payment method*** which does not show any linear correlative relation with the metrics measured.

### Payment Methods Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/f4c8314e-270e-4bee-86f1-ac8092557564)

It was determined that the company offered 2 payment methods, either through the ***App wallet*** or by ***Credit card***. The Choice of payment mathod was found to be almost even between the 2 payment methods

## Revenue Analysis
Pegging the cost of bike usage at **$0.35** per minute, the revenue per trip was calculated by multiplying the usage duration by 0.35. The following insights were drawn from the revenue analysis
* *Total Revenue* = **$2,241,193.76**
* *Minimum Trip Revenue* = **$0.00**
* *Average Trip Revenue* = **$4.31**
* *Maximum Trip Revenue* = **$21.27**

#### Revenue Analysis for Same Start and End Stations Vs Different Start and End Stations
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/76384c86-2c8d-4ee5-863b-7be978b3e0ac)

It was determined that trips with the ***same start and end stations*** were responsible for ***18,134*** trips representing ***3.50%*** of the total number of trips and revenue of ***$43,091.00*** representing ***6.38%*** revenue share, indicating a ***close to double*** the number of trips proportion.

Trips with ***different start and end stations*** had a total number of Trips to be ***501,566*** and revenue of ***$2,098,102.77*** representing ***96.52%*** and  ***93.62%*** respectively.

To identify ***why*** trips with same start and end stations had a ***revenue boom***, it was discovered that the ***average revenue*** from such a trip was ***$7.89*** while the average for trips with different start and end stations was ***$4.18***, indicating a ***longer usage duration*** for trips with same start and end stations 

*This insight can be useful in improving revenue for the company by encouraging users to return bikes to their start stations by rewarding users who do through discount or cashback programs*

## Stations Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/3809c76a-de48-41b7-a22e-8027621704e2)

The top 20 start and end stations, by the number of trips and their revenues are depicted in the plot above. It can be determined that the end stations are slightly busier in terms ending trips than starting trips, although majority of the start and end stations are the same.

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/27a5be3a-3842-41ae-803b-f7dc39464a88)

It was observed that out of the 20 top start and end stations, ***18*** of them were same with ***2*** unique stations from each end on this ranking, indicating the level of engagement at these stations. 

### Comparing the Top 20 Stations to the Rest of the Stations
<div style="display:flex; justify-content:space-between;">
    <img src=https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/bc744cdf-7d0f-4233-bfec-9550c0888428 width="400" height="350"/>
    <img src=https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/0b92c1d7-8493-4e9c-adca-ebe476a13a4e width="600" height="350"/>
</div>


Compared to the remaining ***252*** station, the graphs indicate that despite the ***top 20*** start and end stations comprising ***less than 10%*** of the total number of stations , they account for ***more than 30%*** of the total number of trips and the total revenue made

There may be several ***factors*** contributing to their ***high levels*** of engagement such as ***population of the locality, innovative management, proximity to busy districts, businesses and leisure facilities*** among others. 

To ***improve revenue***, some of these factors can be investigated and ***viable discoveries implemented*** across the other stations or considered when ***establishing new stations***


## Age Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/5acccbf3-12bd-4e5a-a554-646a4c1a18a5)

Categorzing the users into age groups, it was observed that the users, in descending order were in the age brackets of ***31-40, 41-50, 51-60, 21-30*** and ***above 60***

Several speculative assumptions can be made as to why the youngest age group represented such a low proportion of the user such as,
* They are not as active as generations before them, probably caused by easy accessibility as a result of the global digital trasnformation
* Majority may be financially incapable since you may find majority of them being students or unemployed
* Or simply, the locations of the bikes have a low 21-30 age demographic

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/24a812e9-03dc-4d64-8872-6b8c14c92fc5)

From the figure above, it can be seen that for all age groups, the number of subscribers far outnumber the number of customers(non-subscribers), an observation that is similar to the overall subscriber-customer proportions


![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/0211c6a6-3922-4b1c-b84a-30f49c19f883)

Similarly the gender proportions for each age group mimic the overall gender proportions with males users being the most folowed by females and other representing a tiny proportion 

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/574e7915-94f0-4a27-a075-58b7e646c336)

For payment method use, it was realized that across all the age groups, there was no significant difference between app wallet or credit card usage

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/6a26500c-93b1-4260-a8c7-9904727b99d4)

For trip duration, it was realized that the average trip duration was between 10.5 and 12 minutes which does not show much variety in terms of the age groups, which confirm its correlation coefficient of 0.00

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/2e7a75bd-e89e-4351-8386-4e40d2271140)

Breaking the age groups down into the specific genders, it was realized that average trip duration for females of all age groups was 12 minutes and above while males recorded low average trip durations of below 11.7 minutes for all age groups. Other gender also recorded average trip durations within 12 and 13 minutes except for the youngest age group that recorded the lowest duration of below 10 minutes. 

Due to the perfect positive correlation between trip duration, trip distance and trip revenue, the observations were similar as is evident in the figures shown below

<div style="display:flex; justify-content:space-between;">
    <img src=https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/0b29031e-6b3a-444c-8b5a-b0028d9ee651 width="500" height="350"/>
    <img src=https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/f9693c02-99ab-4890-b417-244358c7db5e width="500" height="350"/>
</div>

## Stations Positioning

![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/6f4a92be-098e-4ed9-97b8-00dd3ce0f763)

From the map, it can be seen that the bike renting service has stations clustered in 3 cities, San Francisco, San Jose and Oakland

# Recommendations

* As a service providing company, one way of increasing revenue lies in the area of expansion. From the map, it is obvious that the company has the potential to expand to connecting cites such as Hayward, Freemont, South San Francisco, Daly City, Palo Alto among others, provided similar services are not already present in these cities or the company is ready to compete in the case similar services are already existent in said cities.
* Another means of improving revenue is by offering discount programs and promotions for the youngest age group and below, such as student discounts in a bid to increase users from that age range which translates to more revenue.
* Although females were seen to have the highest average trip duration, female users were far outnumbered by their male counterparts. Implementing schemes that can improve female user numbers is sure going to increase revenue.
* Another area that can be exploited is the payment method. As is usual, credit card payments attract a fee payable by the company, which in turn reduces the revenue per minute as compared to payments made throught the app wallet. Therefore, programs that can increase app wallet payments while decreasing credit card payments is bound to increase company revenue.

## Conclusion

The dataset consisted of 517900 rows, each row representing a bike trip and in extension a user using one of a total of 3673 bikes. 

It was found that males consisted of the majority of users while the average usage duration, time and revenue were higher for females
Also, despite the top 20 start and end stations representing below 10% of the total number of stations(271), it was found that , they were responsible for more than 30% of the total number of trips and revenue. Also, majority of the top 20 start stations were also in the top 20 end stations

In terms of age distribution, majority of the users were in the 31-40 and 41-50 age groups while 21-30 recorded the least number of users
