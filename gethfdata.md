# [GetHFData by Marcelo Perlin](https://cran.r-project.org/web/packages/GetHFData/index.html)

Getting trade data in Brazil is "very difficult." This package
makes it trivial.

## About GetHFData

Cran pkg for importing and aggregating high freq trade data for Brazilian stock exchange

Package works by creating an interface to Bovespa's FTP site

Main points:

Users can download raw or aggregated trade data in one line of code

Choices of tickers and dates are possible

Available data sets:

Equity (spot) trade data and odds lot
Derivatives trade data (options, futures)

## Usage example

```r
library(GetHFData)

last.date <- as.Date('2017-05-14')

#last.date - 90
type.output <- "raw"
my.assets <- c("PETRE15", "PETRF16")
type.market <- "options"

#df.out <- ghfd_get_HF_data(
```

## Next steps

* Implement order data
* Estimats of order book states
* Quoting strategies and intensity
* Interface with highfrequency package
* Distribute whole dat at 5min, 10min, 15min

Book: Processing and Analyzing Financial Data with R
