# Ford-GoBike_Analysis

# About Dataset
The dataset has anonymous information about individual rides made in a bike-sharing system covering the greater San Francisco

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

# Results

## *General Insight into Dataset*
* *Total Number of Trips* - **519700**
* *Total Number of Stations* - **272**
* *Total Number of Bikes* - **3673**

### User Type Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/b0c1f178-eb07-442a-8050-bcb7bc70f943)

Bike users are categorized into 2 groups, ***customers*** who were responsible for ***110470*** trips representing ***21.26%*** of the total number of trips and ***subscribers*** who were responsible for ***409230*** trips representing ***78.74%*** of the total number of trips

### User Gender Analysis
![image](https://github.com/Taingzunaaloung/Ford-GoBike_Analysis/assets/119953557/abeaf08e-dd9f-41b6-8e08-f233a52218ee)

* ***Males*** were responsible for ***348,318*** trips representing ***67.02%*** of the total
* ***Females*** were responsible for ***98,621*** trips representing ***18.98%*** of the total
* ***Other*** were responsible for ***6,299*** trips representing ***1.21%*** of the total
* Bike users who did not specify their gender were categorized as ***Unspecified*** and were responsible for ***66,462*** trips representing ***12.79%*** of the total

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
There may be several ***factors*** contributing to their ***high levels*** of engagement such as ***population of the locality, innovative management, proximity to busy districts, businesses and leisure facilities*** among others. 
To ***improve revenue***, some of these factors can be investigated and ***viable discoveries implemented*** across the other stations or considered when ***establishing new stations***
