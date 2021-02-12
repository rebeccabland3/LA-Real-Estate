Los Angeles Real Estate
						by
						
				   James Milne, Rebecca Bland, Divya Manthena, Katherine Matovic
PROJECT DESCRIPTION AND RESEARCH QUESTION:
What are the top 10 rental neighbourhoods in Los Angeles?

Data Overview
We extracted over 3,300 rows of data from the Mashvisor api (documentation here: https://www.mashvisor.com/api-doc/#introduction), comprising approximately 1,500 rows each for Airbnb and regular rental properties and spanning over 80 neighborhoods. Data download consisted of fields detailing geographic locations of properties e.g. address, city, lat/lng coord, and property specific data including # beds/bths, rewiew counts, occupancy rates (Airbnb), and simple financial data e.g. rental rates by day, week, month etc.

Cleanup and Analysis
We downloaded rental property data from the api for Airbnb and Regular rentals separately, then removed extraneous columns (e.g. room type capacity, amenities etc) and renamed the columns of both datasets so they could be stacked together. Once this was completed, we mapped the existing property type names to a smaller set in order to simplfy our analysis and then ordered/grouped the properties by neighborhood starting with the highest price.  

Python Libraries: Pandas, Matplotlib, Seaborn, scipy.stats, gmap

Interesting Questions/rationale
Where are the properties located on a map of Los Angeles? Any investor would want to see this as a visual.
Are there differences between Airbnb rentals vs Regular? Any investor would want to see this as a visual.
How are the properties grouped by type e.g. house, apartment etc? Any investor would want to see this as a visual.

Findings/Conclusions
