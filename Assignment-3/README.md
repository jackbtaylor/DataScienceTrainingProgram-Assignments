## Intermediate Assignment 3: Working with Categorical Data


#### **Data:** 
We will be using the All-hazards dataset mined from the US National Incident Management System 1999-2020 to explore some relationships between categorical variables in these data. Further information about the dataset can be found [here](https://figshare.com/articles/dataset/All-hazards_dataset_mined_from_the_US_National_Incident_Management_System_1999-2020/19858927/3). Find the dataset and definitions in the assignment folder on the [Teams channel](https://usdagcc.sharepoint.com/:f:/r/sites/FNS-DataScienceTrainingProgram/Shared%20Documents/FY24-25%20Intermediate/Assignments/Intermediate%20Assignment%204%20-%20Working%20with%20Categorical%20Data?csf=1&web=1&e=kZRvqu).

This assignment uses the variables listed below.

-   `START_YEAR` - Start year of incident
-   `TOTAL_PERSONNEL_SUM` - Total personnel resources summed across incident
-   `COMPLEX` - Is fire part of Fire Complex?
-   `FUEL_MODEL` - Primary Fuel Model
-   `POO_STATE` - Point of origin - state


#### **DataCamp:** 

The following DataCamp courses correspond to this exercise:
-   **Python**:
    -   Data Manipulation with pandas
    -   Exploratory Data Analysis in Python
    -   Working with Categorical Data in Python


#### **Assignment:**
1.	**Subset the data to only include incidents:**
    1.	occurring in 2014 or after using the START_YEAR column,
    2.	with at least 10 total personnel using the TOTAL_PERSONNEL_SUM column, and
    3.	retaining only the columns START_YEAR, TOTAL_PERSONNEL_SUM, COMPLEX, FUEL_MODEL, and POO_STATE.
2.	**Check for missing data in the FUEL_MODEL variable.** Are there empty strings, NAs, or NaNs? If there are empty strings, convert them to NA or NaN.
3.	**Create a dataframe of counts for each FUEL_MODEL type.** What fuel type is most common? Which fuel type is the least common? Do you notice anything odd about the categories?
4.	**Create a new factor/category variable from the FUEL_MODEL variable and order the levels by the number of observations in each category using the dataframe created in Step 3.** 
5.	**Use an ordered bar chart (descending) to visualize the counts of FUEL_MODEL observations in your factor/category variables you created in Step 4.** 
6.	**Create a contingency table/cross tabulation of FUEL_MODEL and whether the incident was classified as a complex.** Which fuel type has the highest number of incidents that were categorized as a complex?
7.	**Create a contingency table/cross tabulation of POO_STATE (U.S. state where the point of origin of the incident occurred) and COMPLEX.** What are the states with the most incidents that were classified as a complex? How many states had no incidents classified as a complex?


#### **Deliverables:**
-   Your code (the .R, .Rmd, .py, or .ipynb file).
-   These deliverables will be submitted through GitHub by the end of the program.
