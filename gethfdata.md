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

