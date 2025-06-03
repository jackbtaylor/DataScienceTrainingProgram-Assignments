## Intermediate Assignment 4: Introduction to Regression


#### **Data:** 

Food Environment Atlas with Population 2020.csv

This assignment uses the variables listed below.

-   `GROCPTH16` - Count of grocery stores per 1,000 people, 2016
-   `PCT_LACCESS_POP15` - Percent of households with low access to grocery stores, 2015
- `FFRPTH16` - Count of fast food restaurants per 1,000 people, 2016
- `MEDHHINC15` - Median household income, 2015
- `RECFACPTH16` - Count of recreational facilities per 1,000 people, 2016
- `PCT_DIABETES_ADULTS13` - Adult diabetes rate, 2013
-   `METRO13` - Metro/nonmetro classification, 2013
- `Pop2020` - Census populations on the county level, 2020
* Pop2020 is optional as it comes from the Census API, but is provided as part of the dataset on Teams.

#### **DataCamp:** 

The following DataCamp courses correspond to this exercise:

-   **Python**: Introduction to Statistics in Python
    -   Introduction to Regression with statsmodels in Python
    -   Intermediate Regression with statsmodels in Python

<br><br>

#### **Assignment:**

##### *Part A: Explore correlations*

1.  Subset the data to the list of variables above.
2.  Create histograms of each variable. Do any have skewed distributions? If so, transform them so you are able to detect a stronger correlation (a stronger linear relationship). Examples of transformations can be to standardize, take the log, or take the square root.
3.  Create a correlation matrix with the variables. Which variables are more correlated with each other? Are the correlations positive or negative? What might you expect the relationships to be, and does anything surprise you? Perhaps we are witnessing spurious correlations. Interpret your results accordingly. 
4.  Plot a histogram of `PCT_DIABETES_ADULTS13` and add reference lines for the national mean and median. What causes the mean and median to differ?

##### *Part B: Exploring predictors of diabetes rates*

1.  Take `PCT_DIABETES_ADULTS13` and choose one other variable to do the below analysis.
2.  Create a scatterplot with a text annotation that displays the correlation coefficient.
3.  Run a regression using the two variables, choosing `PCT_DIABETES_ADULTS13` as the response variable.
4. Create a new scatterplot that displays the regression line and its equation.
5. How does this regression satisfy or not satisfy the 5 assumptions of linear regression?
6.  Add `METRO13` to the regression model as a categorical predictor variable. Interpret your results.
7.  Add more variables to the regression model. What are the potential confounders? Are there other variables that may influence the outcome independently?

<br><br>

##### **Deliverables:**

-   Your code (the .R, .Rmd, .py, or .ipynb file).
-   These deliverables will be submitted through GitHub by the end of the program.
