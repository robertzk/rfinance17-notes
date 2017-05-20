# Predicting Loan Deliquency on 1M Rows of Data

Microsoft's David Smith shows us how to operationalize models.

## 

Batch mode:

* Create many (millions!) of predictions at once
* Time required proportional to number of predictions

Realtime:

* Only a few (maybe only one!) data point available to predict
* There may be multiple requests in a short timeframe
* Latency is the key metric here
* Maybe applications require sub-second latency at endpoint

# Real-time operationalization options

* Rewrite prediction code in some other language
* PMML / C++ / Java / ....
* OR, use your R code:
* Deploy as a web service with Microsoft R server
* Deploy as a stored procedure in SQL server

# LendingClub Loan Performance Data

We use the [LendingClub Data](https://www.lendingclub.com/info/download-data.action).
