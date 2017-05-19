# obmodeling

An R pkg which uses xts to manipulate

* Market depth stats
* Price movement, liquidity changes
* Market spread
* Measures of volatility
* PIN/VPIN
* Price pressure
* Trade imbalance

## Setup
```r 
load.quotes(system.file("extdata/ob_quotes.csv", package = "obmodeling"))
load.trades(system.file("extdata/ob_trades.csv", package = "obmodeling"))

Obmodeling uses an environment to store parsed trades and quotes.
`getOB()` to access the env.
Currently supports Reuters data format, more to come.
