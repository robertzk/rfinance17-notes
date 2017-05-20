# Random ideas for connecting syberia with trading

## HFT

To use Syberia for HFT, here's one idea.

* Define a backtesting engine and grammar
* Use it to visualize and test a variety of trading strategies in R
* Define Syberia resources to transpile backtesting strategy from R to VHDL
* Push directly to FGPA array and trade on the wire

In this vision, one team of quants and traders is identifying
optimal trading strategies, and a separate team of "trading data engineers,"
i.e., low-level distributed systems developers are
defining the transpilation layer that creates custom FPGAs
to execute the trading strategies in microseconds.

## Enron email analysis

Based on [Seoyoung Kim's talk](https://github.com/robertzk/rfinance17-notes/blob/master/regtech.md),
it should be possible to use Syberia to make an "email analysis engine":

* Inherit from modeling engine
* Provide standard datasets and import adapters for common anonymized email corpi
* Add text mining feature engineering in lib/mungebits
* Add an "email report" stage to make ggplot2 and/or markdown document

Then you can feed in [arbitrary email data sets](https://www.cs.cmu.edu/~./enron/)
for any organization and correlate against Y (stock price, internal KPI's, etc.)

Happy email data mining!
 
## No bullshit data science

Based off Szilard Pafka's [no bullshit data science talk](https://github.com/robertzk/rfinance17-notes/blob/master/nobullshit.md). Very similar
to [Twitter's paper](http://www.umiacs.umd.edu/~jimmylin/publications/Lin_Kolcz_SIGMOD2012.pdf).
add twitter paper 
* Define a "report and visualization" engine and grammar using controllers and resources.
* Use that engine to replicate Twitter + Szilard's analysis
* Export results as fancy reports, plots, etc. and get invited as a key note speaker to [R finance](http://www.rinfinance.com/)!

"It takes a big man to admit his data is small" - Hadley Wickhan @jcheng
"It's not always the size that matters ;)" - Szilard Pafka
“I really use other people’s code. I can find open source code for what I want to do , and my time is much better spent doing research and feature engineering.” - Owen Zhang

## [Revolution Analytics / Microsoft engine](https://github.com/robertzk/rfinance17-notes/blob/master/loanprediction.md)

All of the ideas in [David Smith's talk](https://github.com/robertzk/rfinance17-notes/blob/master/loanprediction.md) on Loan Prediction in 1M Rows Per Second are easily translatable to Syberia.

* Extend from the modeling engine and call it the "microsoft" engine.
* Define custom import adapters using `rxInput`, etc.
* Mungebits can probably stay the same but they have to fit into the serialized MicrosoftML model object
* Classifiers can come from any `rxLinMod, rxFastLinear,` etc model. 
* Export to a MicrosoftML or SQL Server object into a binary representation or Azure cloud.
* Add a `deploy` global helper to use `library(mrsdeploy)` in lockbox.
* Run R at scale!



