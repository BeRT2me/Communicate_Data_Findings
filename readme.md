# San Francisco Bay Area Bike Share and Weather Exploration
## by BeRT2me

## Dataset
>This Dataset was compiled from two different sources.
>- The first was one of the options provided to me for the project, <b>Ford GoBike System Data.</b>
>- The second was obtained from the National Oceanic and Atmospheric Administration's website, <b>San Francisco Weather Data</b>
>#### Ford GoBike System Data
>- This data, along with basic documentation, can be found <a href='https://www.lyft.com/bikes/bay-wheels/system-data'>here</a>.
>#### San Francisco Weather Data
>- This part of the data used for this project can be found <a href='https://www.ncdc.noaa.gov/cdo-web/orders?id=1901573&email=spam4brt2me@live.com'>here</a>.
>- The documentation for this data can be found <a href='https://www1.ncdc.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf'>here</a>.
>- Precipitation (PRCP) is in mm, Average Daily Temperature (TAVG) is in Degrees Celsius, Average Daily Windspeed (AWND) is in Meters per second.

>### Modifications
> With this raw data, I created a Dataset of daily summaries of the ride-share data, combined with daily weather data for the area. I also created and added the categorical variables of Rainy/Not Rainy, Weekday/Weekend, and Month based on this data.

## Summary of Findings
>#### Variable Distributions
>- The ride duration data is roughly bimodal, centered around 11 and 13.5 minutes.
>- The average daily temperature is bimodal, centered around 13 degrees and 18 degrees. 
>- The average daily windspeed is fairly uniform between 1 and 5 meters per second.
>- The number of rainy days is shows that that category is coded in accordance with normal standards.
>- There is the correct ratio of weekends to weekdays.
>- There are two months of data for every month except May and June, where there is only one month of data for each.
>- Average Birth Year and Percentage of males both are fairly normally distributed. Notably, the percentage of males is greater than 50% at around 75%.

>#### Two Variable Correlations 
>- As the average percentage of males decreases, the average ride duration increases.
>- As temperature increases, the average ride duration increases.
>- Ride duration is shorter when it is rainy.
>- Ride duration is longer on weekends.
>- Ride duration is longer during the summer months.
>
>
>- As the average percentage of males increases, the average birth year decreases.
>- As temperature increases, the average birth year decreases.
>- There is a greater percentage of male riders when it's rainy.
>- There is a greater percentage of male riders on weekdays.
>- There is a lower percentage of male riders during the summer months.
>- Average birth year is lower when it's raining.
>- Average birth year is lower on the weekends.

>#### Three Variable Correlations
> Adding the category of Rainy/Not Rainy:
>- The correlation between temperature and ride duration is only present when it is not rainy.
>- A new correlation; As windspeed increases, ride duration decreases, is only present when it is rainy.
>- A higher average birth year is correlated with a greater percentage of male riders when it is rainy.
>- The correlation between percentage of male riders and average birth year is only present when it is not rainy. 
>
> Adding the category of Weekend/Weekday:
>- The correlation between temperature and ride duration is stronger than before on weekends.
>- A higher average birth year is correlated with shorter ride durations only on weekends.
>- The correlation between percentage of male riders and trip duration is only present on weekends.
>- The correlation between average birth year and percentage of male riders is only seen on weekdays.
>- The correlation between percentage of male riders and temperature is only present on weekends.

## Key Insights for Presentation

> I chose to highlight the three strongest correlations for my presentation:
>1. The correlation between Temperature and Trip Duration on Weekends.
>    * This will be a single well-formatted regplot. 
>2. The correlation between Age and Trip Duration on Weekends.
>    * This will be a single well-formatted regplot.
>    * I will change the average birth year stat to average age for an easier to read graph.
>3. The correlation between Male Rider Percentage and Trip Duration when it is Rainy.
>    *This will be a single well-formatted regplot. 

To view the Presentation:  
`jupyter nbconvert presentation.ipynb --to slides --template output_toggle.tpl
--post serve`