# Los Angeles Rental Market Real Estate
					
by: James Milne, Rebecca Bland, Divya Manthena, Katherine Matovic

## PROJECT DESCRIPTION AND RESEARCH QUESTION:
Our client, a major LA based commercial real estate private investor is looking to add additional rental properties to their portfolio. As part of their preliminary analysis, they have asked to find out: What are the top 10 rental neighbourhoods in Los Angeles and how do they differ for Airbnb vs Regular monthly rental properties?

## Data Overview
We extracted over 3,300 rows of data from the Mashvisor api (documentation here: (https://www.mashvisor.com/api-doc/#introduction), comprising approximately 1,500 rows each for Airbnb and regular rental properties and spanning over 80 neighborhoods. Data download consisted of fields detailing geographic locations of properties e.g. address, city, lat/lng coord, and property specific data including # beds/bths, rewiew counts, occupancy rates (Airbnb), and simple financial data e.g. rental rates by day, week, month etc. We note that Airbnb data was more granular than Regular rental properties, and allowed us to filter on additional data points such as user reviews, occupancy levels etc. 

## Data Scrubbing Methodology
We downloaded rental property data from the api for Airbnb and Regular rentals separately, saved them to csv files and then removed extraneous columns (e.g. room type capacity, amenities etc) and renamed the columns of both datasets so they could be stacked together. Once this was completed, we mapped the existing property type names to a smaller set in order to simplfy our analysis and then ordered/grouped the properties by neighborhood starting with the highest price.  We also added a column comparing monthly prices across Airbnb vs regular rental properties by multiplying nightly rental rates of Airbnb properties by the approximate number of days they would be rented over a month (18 days in a month, computed by observing annual occupancy rate percentages).

## Python Libraries
Pandas, Matplotlib, Seaborn, gmap, csv
gmaps used to plot geographic locations of properties/neighborhoods across LA.  Pandas used for data manipulation. Graphs generated in matplotlib and Seaborn.  

## Research Questions/rationale
We investigated the following questions as a way of exploratory analysis of the data
Where are the properties located on a map of Los Angeles? 
Are there differences between Airbnb rentals vs Regular? 
How are the properties grouped by type e.g. house, apartment etc? 

## Findings/Conclusions
Top 10 neighborhoods are similar to neighborhoods which are most expensive to purchase homes e.g. Bel-Air, Beverly Hills, Pacific Palisades. 
Data is heavily right skewed for both Airbnb and Regular rental properties. Majority of regular renters are spending less than $5,000/mth, while Airbnb renters are spending a bit less than $6,000/mth, slightly higher than renters. Airbnb rentals are taking advantage of demand for rentals in expensive neigborhoods to push up prices over Regular rental properties. At the upper end of the spectrum, properties are 

