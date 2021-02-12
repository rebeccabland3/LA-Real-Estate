Los Angeles Real Estate
						by
						
James Milne, Rebecca Bland, Divya Manthena, Katherine Matovic
PROJECT DESCRIPTION AND RESEARCH QUESTION:
Our client, a major LA based commercial real estate private investor is looking to add additional rental properties to their portfolio. As part of their preliminary analysis, they have asked to find out: What are the top 10 rental neighbourhoods in Los Angeles?

Data Overview
We extracted over 3,300 rows of data from the Mashvisor api (documentation here: https://www.mashvisor.com/api-doc/#introduction), comprising approximately 1,500 rows each for Airbnb and regular rental properties and spanning over 80 neighborhoods. Data download consisted of fields detailing geographic locations of properties e.g. address, city, lat/lng coord, and property specific data including # beds/bths, rewiew counts, occupancy rates (Airbnb), and simple financial data e.g. rental rates by day, week, month etc. We note that Airbnb data was more granular than Regular rental properties, and allowed us to filter on additional data points such as user reviews, occupancy levels etc. 

Cleanup and Analysis
We downloaded rental property data from the api for Airbnb and Regular rentals separately, saved them to csv files and then removed extraneous columns (e.g. room type capacity, amenities etc) and renamed the columns of both datasets so they could be stacked together. Once this was completed, we mapped the existing property type names to a smaller set in order to simplfy our analysis and then ordered/grouped the properties by neighborhood starting with the highest price.  We also added a column which enabled us to compare monthly prices across Airbnb and regular rental properties by multiplying nightly rental rates of Airbnb properties by the approximate number of days they would be rented over a month (using annual occupancy rate percentages)

Python Libraries: Pandas, Matplotlib, Seaborn, gmap, csv
gmaps used to plot geographic locations of properties/neighborhoods across LA.  Pandas used for data manipulation. Graphs generated in matplotlib and Seaborn.  

Interesting Questions/rationale
Where are the properties located on a map of Los Angeles? Any investor would want to see this as a visual.
Are there differences between Airbnb rentals vs Regular? Any investor would want to see this as a visual.
How are the properties grouped by type e.g. house, apartment etc? Any investor would want to see this as a visual.

Findings/Conclusions
