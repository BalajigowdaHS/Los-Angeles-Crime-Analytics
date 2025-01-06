# Exploring Crime Trends in Los Angeles (2020-2023)

## Overview

The dataset, sourced from the website https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-Present/2nrs-mtv8/about_data, compiles crime data in the city of Los Angeles from 2020 to the present, offering a comprehensive record of public safety incidents. With a substantial dataset of 843515 records, each row captures details of specific crimes, while the 28 columns provide a wealth of information including incident dates, locations, crime types, victim demographics, and investigative status. This dataset serves as a valuable resource for analyzing and understanding the dynamics of criminal activity in Los Angeles over the specified timeframe


## Why is important and what appeals to you about it

The importance of a dataset often lies in its relevance to a specific research question or analytical goal. If the dataset covers a wide range of crime incidents in Los Angeles from 2020 to 2023 November, it could be crucial for studying crime patterns, identifying trends, and informing public safety strategies.

Datasets that provide a comprehensive view of a phenomenon, such as crime incidents, are valuable. The dataset you are using covers a significant period (from 2020 to 2023 November) and includes a large number of records (854k), making it potentially rich in information for various analyses.

A dataset's appeal often stems from the diversity of variables it includes. The crime dataset contains many columns, covering aspects like date and time of occurrence, location, crime types, victim demographics, and more. This diversity allows for a nuanced exploration of crime-related factors.

The dataset is geographically focused and specific to the city of Los Angeles. This can be advantageous for local policymakers, law enforcement agencies, and researchers seeking insights into crime dynamics within that particular region.


## Is this dataset suitable for dimensional modeling and analytical analysis?


Due to its structured format and granular data, the crime dataset is suitable for dimensional modeling and analytical analysis. With key dimensions like time and location, along with fact and dimension tables, the dataset allows for a comprehensive exploration of crime patterns. The inclusion of temporal information supports the creation of a time dimension for time-based analysis. Overall, these characteristics make the dataset well-suited for in-depth analytical investigations into crime trends and patterns.


![Fact and Dimensions](https://github.com/user-attachments/assets/b3f85695-082d-436a-9dec-cae93857b55e)



## Problem Statement

Crime data in Los Angeles is vast and complex, encompassing different dimensions such as time, location, victim demographics, crime types, and investigative statuses. The challenge lies in identifying actionable insights to reduce crime rates and improve community safety.

This project addresses this challenge by answering the following key business questions.


## How has the overall crime rate in the city evolved over the past few years?

To effectively analyze the evolution of the city's overall crime rate over the past few years, our approach involves a multi-dimensional examination of the available crime data. Firstly, we focus on the annual aggregation of crime incidents, providing a clear picture of the year-over-year changes in crime rate. This broad perspective is crucial to understand the general trend, whether there's an increase or decrease in criminal activities over the years.

Furthermore, to gain a deeper understanding of seasonal and monthly variations in crime patterns, we dissect the data into more granular time segments. By breaking down the crime statistics by quarters and months within each year, we can identify specific periods that demonstrate a notable increase or decrease in crime rates. Such detailed analysis enables us to pinpoint times of the year when the city experiences higher criminal activities, potentially correlating these periods with various socio-economic factors or seasonal events.

![image](https://github.com/user-attachments/assets/724f2872-fe1b-4552-992c-7802bbc63017)


The data reveals a fluctuating trend in total crimes during this period. In 2020, there were 199,470 reported crimes, which increased to 209,440 in 2021. The year 2022 saw the highest number of reported crimes at 234,401, followed by a slight decrease to 204,414 in 2023.

Then, we use this SQL query to calculate the total number of crimes for each quarter of each year, by joining our fact table with the date table and grouping the results by both year and quarter.

### Summary of Quarterly Crime Data:

The data reveals the total crimes for each quarter over four years, offering insights into seasonal trends and year-over-year changes in crime rates.
Analysis of Yearly and Seasonal Trends:

2020: Showed a gradual decrease in crime rates from the first to the fourth quarter.
2021: Started with slightly lower crime numbers than the same period in 2020, but saw a steady increase in each subsequent quarter, peaking in Q4.
2022: Marked the highest crime rates across all quarters compared to the previous years, with a notable peak in Q2.
2023: Demonstrated fluctuating crime numbers in the first three quarters, with a significant drop in Q4 because the data is available till October only.
Interpretation and Implications:

The consistent rise in crime rates in 2021 and the peak in 2022 suggest an escalating trend in criminal activities or changes in socio-economic conditions during these periods.
The significant decrease in crimes in the fourth quarter of 2023 might indicate the effectiveness of crime prevention measures or a change in external factors impacting crime rates.
The data highlights the need for seasonal and quarter-specific crime management strategies and resource allocation strategies.

![image](https://github.com/user-attachments/assets/d5a9841d-91a4-4462-a416-8d259c89272e)

### Identification of Peak Crime Months:

The analysis begins by listing the months with the highest crime rates in 2022, providing specific figures for each month to illustrate the data clearly.
Each month is presented alongside its total crime count, giving a detailed view of when criminal activities were most prevalent.
Observation of the Most Affected Months:

After enumerating the monthly data, the text highlights that May, October, and June are among the months with the highest crime rates.
This observation is important to identify specific periods within the year when the city experienced the most criminal activities.
Analysis and Interpretation of Trends:

The analysis interprets these findings, suggesting that certain months, notably May and October, might have specific conditions or events that lead to higher crime rates.
It posits that these periods could be significant for law enforcement agencies for strategic planning and resource allocation.
Additional Insights and Broader Implications:

Beyond identifying the peak months, the analysis notes that the crime rates in other months like July, December, and April were also relatively high, though not the highest.
This indicates a need for a continuous and adaptive approach to crime prevention and public safety throughout the year.
Conclusion:

The concluding remark synthesizes the analysis, stating that the monthly crime data of 2022 reflect significant variations in criminal activities across different times of the year.

![image](https://github.com/user-attachments/assets/c3aebbd0-d17a-42c9-b2ba-6c5b1e32d66f)


## What are the top 10 types of crimes that have been solved and unsolved?

I chose to explore this question within the dataset because understanding the resolution status of different types of crimes is crucial for public safety and law enforcement efficiency. Analyzing solved and unsolved crime cases allows us to delve deeper into crime patterns, thereby providing data support for optimizing law enforcement strategies and effectively allocating public resources.

To answer this question, we conducted a series of database query analyses, focusing on two key aspects:

1) Identified the top 10 types of crimes with the highest number of solved and unsolved cases;
2) Further investigate which cases within these crime types have been resolved and which remain open.

![image](https://github.com/user-attachments/assets/5f3c621b-0ab6-4f49-b021-35c9b3045fa4)

![image](https://github.com/user-attachments/assets/a5eb3e2a-e6e8-4a4d-82a8-99d31bbd82b6)

![image](https://github.com/user-attachments/assets/c1f985e2-5d9d-4094-8f33-fd0d2dd5a468)

## How many crimes were solved each year?

In the analysis of solved crimes over the past four years, the data reveals a varying trend. The highest number of crimes solved was observed in 2020, with 47,751 cases, followed by 2021 and 2022, each with 45,854 and 44,790 cases, respectively. However, there was a noticeable drop in solved crimes in 2023, reaching 29,994 cases. This information highlights the annual fluctuations in the effectiveness of law enforcement efforts in resolving reported crimes.

![image](https://github.com/user-attachments/assets/c5a0c3dd-1f0a-424b-9a52-f1c674bd1417)



## What is the distribution of total crime victims across different age groups? What are the top 3 crimes and their counts for each age group of the victims?

I embarked on this inquiry not only to reveal the prevalence of victimization across different age groups but also to uncover the specific types of crimes that predominantly affect each group. 

- Initially, aimed to determine the distribution of crime victims across various age brackets. This involved analyzing the total number of victims in each age category to observe any emerging patterns or trends.
  
- Subsequently, endeavored to identify the top three crimes within each age group, along with their respective counts.
![image](https://github.com/user-attachments/assets/d6613092-9215-48a1-a9e4-e13aaa00e154)

## Which areas or neighborhoods have the highest and lowest crime rates?

Our group aims to contribute to the resolution of societal issues and enhance community safety and social equity by researching areas with the highest and lowest crime rates. This study holds significant importance for policymakers, social workers, and criminologists alike.

### Top 7 Crime Areas

![image](https://github.com/user-attachments/assets/80a524f7-ff61-475c-a7a1-aac4a922084a)

In the specified locations, the highest reported total crimes are in the "Central" area with 57,280 incidents, followed by "77th Street" with 53,324 incidents, and "Pacific" with 49,502 incidents. Other areas with significant crime counts include "Southwest" (47,581), "Hollywood" (44,790), "Southeast" (43,127), and "Olympic" (42,732).

### Bottom 7 Crime Areas
![image](https://github.com/user-attachments/assets/b0019f3d-cada-49eb-935e-c079306b1970)

## Top Crime areas by years
![image](https://github.com/user-attachments/assets/9f9b1116-3bad-4f79-a0ce-988a9031e4ee)

### Crime Type Dominance by Area

![image](https://github.com/user-attachments/assets/04d87d14-a808-4b73-8c60-1a90ca27accc)

1. **High Crime Areas**:
   - The areas 'Central', '77th Street', and 'Pacific' were identified as having the highest crime rates. These areas consistently showed elevated levels of criminal activities.

2. **Low Crime Areas**:
   - Conversely, 'Foothill', 'Hollenbeck', and 'Mission' emerged as neighborhoods with the lowest crime rates. This indicates a relatively safer environment in these areas.

3. **Yearly Trends in High Crime Areas**:
   - An analysis of yearly crime trends in the high crime areas revealed that 'Central' and '77th Street' had consistently high crime rates across the years. Notably, 'Central' experienced a significant spike in crime in 2022.

4. **Dominant Crime Types**:
   - In terms of crime types, 'VehicleStolen' was the most common crime in many areas, suggesting a city-wide issue with vehicle theft. However, some areas like 'Hollywood' and 'Topanga' showed different patterns, with 'Battery - Simple Assault' and 'Burglary' being more prevalent.
  
## The most common types of crimes and their variations across different areas can vary significantly

1. **Theft and Burglary:**
   - Theft, including petty theft under 950 and grand theft over 950, is a common crime in many urban areas.
   - Burglary, which involves breaking and entering a building with the intent to commit a crime, can occur in both residential and commercial areas.
   - The frequency of theft and burglary may vary based on the economic status of the neighborhood. Higher-income areas may experience fewer thefts, while lower-income areas may have higher rates.

2. **Assault and Battery:**
   - Simple assault and battery are common crimes in urban areas, often occurring in public places like streets, bars, and nightclubs.
   - Aggravated assault, which involves the use of a deadly weapon or causing severe injury, may be more prevalent in areas with higher crime rates.

3. **Robbery:**
   - Robbery, the act of taking property from someone using force or the threat of force, is more likely to occur in areas with higher population density.
   - Commercial areas, such as shopping malls and convenience stores, may be prone to robberies.

4. **Vandalism:**
   - Vandalism, which includes damage to property like graffiti and destruction of public facilities, can occur in both urban and suburban areas.
   - Areas with more public infrastructure may experience higher rates of vandalism.

5. **Identity Theft:**
   - Identity theft is a white-collar crime that can happen anywhere, often involving the theft of personal information for financial gain.
   - It can occur both online and offline, making it a widespread issue.

6. **Vehicle-Related Crimes:**
   - Vehicle theft and burglary from vehicles are common in areas with a high volume of parked cars, such as residential neighborhoods and parking lots.
   - Carjacking, a more violent crime, can happen in any area but may be more prevalent in certain neighborhoods.

7. **Drug-Related Offenses:**
   - Drug-related crimes, including possession and distribution, can occur in various areas, but drug hotspots may exist in neighborhoods with drug-related issues.

8. **Sexual Assault:**
   - Sexual assault can happen in any location but may be more prevalent in areas with nightlife, college campuses, or isolated areas.

9. **Domestic Violence:**
   - Domestic violence cases can occur in residential areas and may not always be reported to law enforcement.

10. **White-Collar Crimes:**
    - White-collar crimes like fraud, embezzlement, and money laundering can happen in business districts and corporate environments.

