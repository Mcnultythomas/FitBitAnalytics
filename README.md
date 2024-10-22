Title: # FitBitAnalytics data-prepartion

Data Source: https://www.kaggle.com/datasets/arashnic/fitbit 

Since the data set starts out separated by month into two sets of csv files, the first step of this process was to combine each respective metric. That way there is only one data set, which makes for a cleaner data structure. Specifically it makes easier to check for duplicates/missing data, ensures consistency in the table names and data formatting, and lastly makes the querying easier and simpler.  

Before importing data into MySQL Workbench I went through each csv file to check for data validity by doing the following: 

Check and remove any duplicates for each tables data sets.  

Ensure formatting and data synchronicity across each combined data set. 

Create columns where needed (ie creating a month column). 

Uploading the clean data into MySQL workbench, and ensure data loads in/look correctly.  

For ease of life, I initially used the 'table data import' on my MySQL application available, MySQL Workbench when available. 

 

Week of 10.6.2024 

Running a few basic test queries to make sure all data is importing correctly. So far so good, excluding the table ‘hourlysteps_merged_total’ where the hour time did not correctly import over. This required another review and reformatting of the csv file and import. When removing duplicates -175 were found and removed, and formatting for the date column labeled ‘Activity Hour’ was reformatted to yyyy-mm-dd hh:mm. 

For weightLogInfo_merged_total, only two duplicates were found and removed. 

[Please note prior to this project I set up my local MySQL server connection.] 

Current tables:  

`fit_bit_project`.`dailyactivity_merged_total`, `fit_bit_project`.`hourlycalories_merged_total`, `fit_bit_project`.`hourlyintensities_merged_totals`, `fit_bit_project`.`hourlysteps_merged_total`, `fit_bit_project`.`minutesleep_merged_total`,  
`fit_bit_project`.`weightloginfo_merged _total` 

 
