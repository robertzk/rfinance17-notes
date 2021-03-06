# [PortfolioAnalytics](https://cran.r-project.org/web/packages/PortfolioAnalytics/index.html) tutorial

by Ross Bennett.

## Intro

Restricted to domestic equity large and midcap stocks

## Factor Zoo

Lots of factors have come out in top journals in recent years. 59 discovered between 2010
and 2012. (Harvey, Liu, and Zhu 2015)

Criteria:

* Substantiated by research
* Demonstrated historical return premium 
* Investable and defined with a systematic, rules based approach

Top are:

* Market, Size, Value, Momentum, Yield, Volatility, Quality, and Liquidty

## Single factor indexes are not all equal

Qualitative features

* Similar factor defs but unique index construction process across providers
* Different universe of assets depending on provider and parent index

Quantitative features

* Risk and return characteristics
* Caveat of reling on historical backtest data, several of the indices
  have less than 5 years of live performance data.

Spoiler: NO! Do you own due diligence.

## Missed slides

Some graphs and things on portfolio optimization I wasn't able to catch.

Idea: Smooth out cyclical nature of single factor indices to make
a composite index.

## Portfolio optimization

```r
library(PortfolioAnalytics)
R.4f <- R[, four.factor]
rp.seq <- generatesequence(min = 0, max = 1, by = 0.001)
port.spec <- portfolio.spec(assets = colnames(R.4f), weight_seq = rp.seq)
# some missed
```

Let's add some objectives.

```r
# minimum standard deviation portfolio
port.min.sd <- add.objective(portfolio = port.spec, type = "risk", name = "StdDev")

# 4 other examples on slides:
# minimum expected shortfall (type = "risk", name = "ES")
# component contribution to risk (standard deviation) (type = "risk_budget", name = "StdDev")
# component contribution to risk (expected shortfall) (type = "risk_budget, name = ""ES")
# constant relative risk aversion (type = "return", name = "CRRA")

Key of package is that it handles multi-objective problems very well.
```

## Portfolio optimization: CRRA

Fourth order expansion of the constant relative risk aversion utility function
as in Martellini and Ziemann (2010) and Boudt, Lu and [didnt catch].

"An objective function is any valid R function. Just have to hand it to the optimizer
and go find me the thing that minimizes or maximizes it."

## Run optimizer

```r
# Uses the following functions from pkg, missed rest of slides
optimize.portoflio.rebalancing
normalizeWeights
Return.portfolio
```
Optimal weights plot:

```r
chart.Weights(...)

```

4-factor performance summary:

```r
charts.PerformanceSummary(cbind(R.min.sd, R.min.es, R.erc.es, R.crra, R.rf), ...)
```

## Slide on 4Factor vs 6Factor

Missed.

## Portfolio simulation

Find no-skill managers:

* Random portfolios to simulate portfolios of zero skil managers
* Feasible portfolios by consturction
* Monte Carlo requires a model spec
* Time series dependency with bootstrap
* No gurantee of a feasible portfolio with bootstrap or monte carlo
* Understand impact of constaints

Graph with simulation performance summary.

## Conclusion

* Bottom up optimization
* Better estimates and forecasts
* Factor timing

Tools available to apply quantitive rigor.

Do your due diligence!

