# MSDS_DataMining
# Lab1
# By Chiranjeevi Mallavarapu, Nitya Doss, Ramesh Simhabhatla, Ramya Mandava

##### Business Understanding ########


The IRS-990 dataset originates from United States Internal Revenue Service (IRS). The data includes financial information
of non-profit/exempt organizations. For the purpose of this project, the dataset is selected from google public datasets at
https://cloud.google.com/bigquery/public-data/irs-990 which makes it queryable easily. The datasets are further narrowed down 
to only organizations that filed during the year 2016 in order to get active organizations. IRS spends millions of dollars 
every year in the processing efforts of paper filing[1]. Properly predicting how many organizations would do paper filing vs 
electronic filing is a question of interest to IRS on an yearly basis. Even IRS website gives this as one of its top 
guidelines yearly during filing time[2]. We would like to come up a logistic model that can predict this outcome. We would 
like to use ROC curves to determine the prediction accuracy. 

Our scope started with 72 variables and 500,000 records across all states of america including Canada. We used scatter plots 
with indicator variables for type of filing to determine most statistically significant variables. Per above exercise we could
narrow down the list to 25 variables.

[1]http://www.nextgov.com/technology-news/2009/09/irs-continues-to-pay-millions-to-process-paper-tax-returns/44867/
[2]https://www.irs.gov/newsroom/avoid-common-tax-filing-errors-irs-encourages-efiling-careful-review


#######################################
