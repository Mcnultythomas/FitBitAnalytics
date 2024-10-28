Title: # FitBitAnalytics data-prepartion

Data Source: https://www.kaggle.com/datasets/arashnic/fitbit 

Introduction: This passion project is an analytical deep dive into a group of individuals health metrics over the course of a month. Specifically, this project will utilize MySQL querying (INNER JOINs/LEFT RIGHT/ FULL JOINs, Aggregations, SubQueries, etc.) to show any meaningful connections and possible impactful actions followed by the visualization and reporting of those results with Tableau. github repository organization plan [estimated 5 branches]

DATA PREPARATION/CLEANING DOCUMENTATION:

For ease of life, I initially used the 'table data import' on my MySQL application available to me, MySQL Workbench.
[Please note prior to this project I set my local MySQL server connection.]

Current SQL synbtax for testing data being adding into database:
USE fit_bit_project;

/*SELECT hourlycalories_merged_total.Id, max(hourlycalories_merged_total.Calories) as "max_calories"
FROM hourlycalories_merged_total
GROUP BY hourlycalories_merged_total.Id
ORDER BY max_calories DESC
LIMIT 5;*/

/*SELECT dailyactivity_merged_total.Id, max(dailyactivity_merged_total.TotalSteps) as "max_steps"
FROM dailyactivity_merged_total
GROUP BY dailyactivity_merged_total.Id
ORDER BY max_steps DESC;*/

/*SELECT *
FROM dailyactivity_merged_total
LIMIT 5;*/

/*SELECT *
FROM hourlycalories_merged_total
LIMIT 5;*/

/*SELECT *
FROM hourlyintensities_merged_totals
LIMIT 5;*/

/*SELECT *
FROM hourlysteps_merged_total
LIMIT 5;*/

/*SELECT *
FROM minutesleep_merged_total
WHERE minutesleep_merged_total.date > "2016-03-15 02:39:00"
LIMIT 5;*/

SELECT *
FROM weightloginfo_merged_total
LIMIT 5;
