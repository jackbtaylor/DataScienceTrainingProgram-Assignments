# Intermediate Assignment 1: Importing and Joining Data

## Data: 
- USDA ERS Food Environment Atlas Dataset: [download here from DSTP Teams](https://usdagcc.sharepoint.com/:x:/r/sites/FNS-DataScienceTrainingProgram/Shared%20Documents/General/Datasets/Food%20Environment%20Atlas.xlsx?d=w93c81e86816c4bc2a6f8ea4b744914c3&csf=1&web=1&e=vIkINh)
- 2020 Census data on population by county: query from Census API in Part 2 of the assignment

## DataCamp: The following DataCamp courses correspond to this exercise:
### R 
- Introduction to Importing Data in R
- Intermediate Importing Data in R
- Data Manipulation with dplyr
- Joining Data with dplyr
### Python 
- Introduction to Importing Data in Python
- Intermediate Importing Data in Python
- Data Manipulation with Pandas
- Joining Data with Pandas

## Assignment:

### Part 1: Food Environment Atlas
1. Save the Food Environment Atlas to a new folder on your computer that you will be using for the assignment.
2. Open the file in Excel to explore the dataset. You can also learn more about the dataset on the [ERS website](https://www.ers.usda.gov/data-products/food-environment-atlas/).
3. Load the necessary packages into your environment in order to be able to import/read in an .xlsx file, and import the Food Environment Atlas file to your environment.
4. There are 13 sheets in the file. 9 of them are: ACCESS, STORES, RESTAURANTS, ASSISTANCE, HEALTH, INSECURITY, TAXES, LOCAL, SOCIOECONOMIC. Merge these 9 sheets using together using unique [county FIPS codes](https://www.census.gov/programs-surveys/geography/guidance/geo-identifiers.html) to make a dataset called EnvironmentAll.

### Part 2: Query Census API
1. Load in the county population data for the 2020 Census using the Census API. The data will come in a JSON format rather than a .csv or dataframe. Use the following API URL: https://api.census.gov/data/2020/dec/pl?get=P1_001N&for=county:*
2. Convert the JSON object into a dataframe called Census2020Pop and rename the variables.
3. Create a unique county FIPS variable by concatenating the string variables for state FIPS codes and county FIPS codes. For example, if state=”01” and county=”01”, your FIPS variable should be FIPS=”01001”.

### Part 3: Combine Datasets
1. Merge the EnvironmentAll and Census2020Pop datasets on the county FIPS codes.
2. Print out the number of columns in each dataset as proof of a successful data merge.

### Bonus:
- Are there a different number of observations between the EnvironmentAll, Census2020Pop, and final merged datasets? Which counties appeared in only one dataset and not the other?

## Deliverables:
- Your code (the .R, .Rmd, .py, or .ipynb file)

## Appendix
Below is the API URL for this exercise and a description of the structure of the query.
https://api.census.gov/data/2020/dec/pl?get=P1_001N&for=county:*
- **2020/dec/pl?** this lists the dataset we want to query. In this case, it is the Redistricting Data (PL 94-171) dataset from the 2020 Decennial Census. See [Decennial Census (2020, 2010, 2000)](https://www.census.gov/data/developers/data-sets/decennial-census.html)
- **get=** this is a function that allows you specify the variables you want to request. Include this in the API URL before listing the variables.
- **P1_001N** this is the variable we are requesting. It represents total population. A list of the variables in this dataset can be found here [2020 PL API Variables](https://api.census.gov/data/2020/dec/pl/variables.html), and this link can be found on the [Decennial Census (2020, 2010, 2000)](https://www.census.gov/data/developers/data-sets/decennial-census.html) page under Redistricting Data (PL 94-171).
- **&for=** this is a predicate which allows you to filter the resulting data by desired geographic level and specific geographies.
- **&for=county:\*** will provide data for each county

For more information on Census API queries, see [Introduction to the Census Bureau Data API](https://www.census.gov/data/academy/courses/intro-to-the-census-bureau-data-api.html) “Part 2: Core Concepts of the Census Bureau Data API”
