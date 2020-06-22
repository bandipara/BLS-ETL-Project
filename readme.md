# Team:
Maria-Elena Gorini, Bhargav Andipara, Bhoomika Patel , Saniya Sule.

## Extraction:

### Data Sources:
#### Bureau of Labor: https://www.bls.gov/ 
#### Zillow: https://www.zillow.com/

### Granularity:
Geography: by County/State  
Years: 2015 to 2018

### Format:
•	API  
•	CSV   
•	TEXT


## Transformation:
Our first steps in cleaning up the datasets involved figuring out which variables were irrelevant and cleaning up the data

1. CSV - We merged the data for years and concatenated it. Created a new data with the required columns. 

2. Zillow API -XML Data extract from Zillow. Transformed into JSON using `xmltodict` library in python.

3. BLS API – We extracted data from BLS through API and stored and created to data frame for Total, employment and unemployment and then created the data frame.

## Load:
The last step was to transfer our final output into a Database. We created a database and respective tables in PostgreSQL. 
We queried the data using `SQL script` in PostgreSQL and in python using `sqlalchemy` library.

![](/Images/flowchart.PNG)


## Summary
The objective of this ETL is to extract and merge information of Wages, Employment, Unemployment and Median House Prices for each county of New Jersey. The final output has the tables for:

•	Civilian labor Population  
•	Unemployment and Employment   
•	Median Household Income  
•	Median house prices  

![](/Images/DBDimage.PNG)


