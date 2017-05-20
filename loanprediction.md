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

# Operationalization with Microsoft R Server

Data scientist publishes R function into web services.
IT administration configures Microsoft R Server for
operationalizing R analytics. Configures a data science
virtual machine, Azure GS5 instance, 32 cores, 448GB RAM.

Then for consumption, we explore and consume services in R directly
using the mrsdeploy package. Or we can integrate with apps using
Swagger API service and consume with any programming language.

# Some examples 

An R intepreter is spawned on-demand using Swagger via REST API

```r
library(mrsdeploy)
publishService(serviceType = "Script", Code = "R script or Function")
publishService(serviceType = "RealTime", model = "R object")
```

RevoScaleR or MicrosoftML models.
Prediction engine.

Realtime Deployment Models:

* Linear Regression (rxLinMod, rxFastLinear)
* Logistic Regression (rxLogit, rxLogisticRegression)
* Classification / Regresion (rxDTree, rxFastTrees)
* Classification / Regression forests (rxDForest, rxFastForest)
* Stochastic boosting gradients
* Etc.

# R studio integration

```r
library(RevoScaleR)
conStr <- "Driver string"
ds <- RxSqlServerData(sqlQuery = "SELECT revol, ....")
df <- rxImport(ds)
rxSetComputeContext("local")
dxForestModel <- rxDForest(is_bad ~ revol_util + ..., df)

# Or train model remotely:
sqlCC <- RxInSqlServer(connectingString = conStr)
rxSetComputeContext(sqlCC)
dForestModel <- rxDForest(is_bad ~ ..., ds)

# Deploy model object and publish flexible and realtime services
library(mrsdeploy)
remoteLogin("http://foo:12800", username = "...", password = "...")
pause()

putLocalObject("dForestModel")
```



