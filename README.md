## Exploring Crime Trends in Los Angles (2020-2023)


The dataset, sourced from the website https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-Present/2nrs-mtv8/about_data, compiles crime data in the city of Los Angeles from 2020 to the present, offering a comprehensive record of public safety incidents. With a substantial dataset of 843515 records, each row captures details of specific crimes, while the 28 columns provide a wealth of information including incident dates, locations, crime types, victim demographics, and investigative status. This dataset serves as a valuable resource for analyzing and understanding the dynamics of criminal activity in Los Angeles over the specified timeframe

Significant trends have emerged in a thorough examination of crime data spanning 2020-2023, offering valuable insights into reported incidents.

#### How has the overall crime rate in the city evolved over the past few years?

To effectively analyze the evolution of the city's overall crime rate over the past few years, our approach involves a multi-dimensional examination of the available crime data. Firstly, we focus on the annual aggregation of crime incidents, providing a clear picture of the year-over-year changes in crime rate. This broad perspective is crucial to understand the general trend, whether there's an increase or decrease in criminal activities over the years.

Furthermore, to gain a deeper understanding of seasonal and monthly variations in crime patterns, we dissect the data into more granular time segments. By breaking down the crime statistics by quarters and months within each year, we can identify specific periods that demonstrate a notable increase or decrease in crime rates. Such detailed analysis enables us to pinpoint times of the year when the city experiences higher criminal activities, potentially correlating these periods with various socio-economic factors or seasonal events.

The data reveals a fluctuating trend in total crimes during this period. In 2020, there were 199,470 reported crimes, which increased to 209,440 in 2021. The year 2022 saw the highest number of reported crimes at 234,401, followed by a slight decrease to 204,414 in 2023.

Then, we use this SQL query to calculate the total number of crimes for each quarter of each year, by joining our fact table with the date table and grouping the results by both year and quarter.

#### Summary of Quarterly Crime Data:

The data reveals the total crimes for each quarter over a four-year period, offering insights into seasonal trends and year-over-year changes in crime rates.
Analysis of Yearly and Seasonal Trends:

2020: Showed a gradual decrease in crime rates from the first to the fourth quarter.
2021: Started with slightly lower crime numbers than the same period in 2020, but saw a steady increase in each subsequent quarter, peaking in Q4.
2022: Marked the highest crime rates across all quarters compared to the previous years, with a notable peak in Q2.
2023: Demonstrated fluctuating crime numbers in the first three quarters, with a significant drop in Q4 because the data is avaliable till october only.
Interpretation and Implications:

The consistent rise in crime rates in 2021 and the peak in 2022 suggest an escalating trend in criminal activities or changes in socio-economic conditions during these periods.
The significant decrease in crimes in the fourth quarter of 2023 might indicate the effectiveness of crime prevention measures or a change in external factors impacting crime rates.
The data highlights the necessity for seasonal and quarter-specific strategies in crime management and resource allocation.

#### Identification of Peak Crime Months:

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


### What are the top 10 types of crimes that have been solved and unsolved?

Our team chose to explore this question within the dataset because understanding the resolution status of different types of crimes is crucial for public safety and law enforcement efficiency. Analyzing solved and unsolved crime cases allows us to delve deeper into crime patterns, thereby providing data support for optimizing law enforcement strategies and effective allocation of public resources.

To answer this question, we conducted a series of database query analyses, focusing on two key aspects:

we identified the top 10 types of crimes with the highest number of solved and unsolved cases;
we further investigated which cases within these crime types have been resolved and which remain open.
