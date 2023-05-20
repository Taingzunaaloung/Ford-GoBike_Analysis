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
### Univariate Analysis

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
