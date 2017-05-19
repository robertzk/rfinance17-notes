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
Use `getOB()` to access the env. Currently supports Reuters data format, more to come.

## Calling functions

```r
head(effective.spread("ESH6", store = TRUE), 2)
ob <- getOB()
names(ob$ESH6)
```

## Current functions

```r
bidask.changes
effective.spread
load.quotes
load.trades
market.depth.stats
quoted.spread
ticks.wide
trade.imbalance
trade.size.stats
```

## Visualize Order Book
```r
chart.dpeth("ESH6")
```

Insert nice little graph.

## Future analysis

* Market toxicity
* Event analysis


## Install

devtools::install_github("jmazar/obmodeling")
