# MSDS_DataMining
# Lab1
# By Chiranjeevi Mallavarapu, Nitya Doss, Ramesh Simhabhatla, Ramya Mandava

##### Business Understanding ##############


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
narrow down the list of variables to 26. We then used random sampling to narrow down the records to 50,000.

[1]http://www.nextgov.com/technology-news/2009/09/irs-continues-to-pay-millions-to-process-paper-tax-returns/44867/
[2]https://www.irs.gov/newsroom/avoid-common-tax-filing-errors-irs-encourages-efiling-careful-review


##### Data Meaning Type #################

Following are the 26 selected variables.

Field				Type		Description
ein					Num			Employer Identification Number
elf					Char		E-file indicator [Prediction variable]
name				Char		Primary Name of Organization
street				Char		In Care of Name
city				Char		City
state				Char		State
zip					Char		ZIP
affiliation			Num			Affiliation Code
deductibility		Num			Deductibility Code signifies whether contributions made to an organization are deductible
activity			Num			These are codes which reflect an organization's purposes, activities, operations, or type. From one to three activity 									codes may be in this field. Note: activity codes became obsolete with the adoption of the National Taxonomy of Exempt 									Entity (NTEE) coding system in January 1995. However, organizations determined to be exempt prior to that date will 									reflect the activity codes previously assigned. 
organization		Num			Organization Code
asset_cd			Num			Asset Codes relate to the book value amount of assets show 
income_cd			Num			Income Codes relate to the amount of income shown on the most recent Form 990 
filing_req_cd		Num			This indicates the primary return(s) the organization is required to file. 
acct_pd				Num			This designates the accounting period or fiscal year ending date (Jan - Dec) of the organization (MM). 
asset_amt			Num			Asset Amount is the Book Value Total Assets End of Year 
revenue_amt			Num			Amount from Form 990 

tax_pd				Char		Tax period
subseccd			Char		Subsection code
totrevnue			Num			Total revenue
totliabend			Num			Total liabilities -- eoy
filedf990tcd		Char		Form 990-T filed?
gftgrntsrcvd170		Num			Gifts grants membership fees received (170)
grsrcptsrelated170	Num			Gross receipts from related activities (170)
exceeds1pct509		Num			Amount support exceeds total (509)
grsinc509			Num			Gross income from interest etc (509)

#######################################
