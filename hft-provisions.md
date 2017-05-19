# Revealing HFT provisions of Liquidity with Visualization in R

By Michael Hirsch.

We'll be looking at the liquidity provisions for HFTs.

## Overview

* Liquidity provision over time of HFTS
* Long-term liquidity provision
* Flurries in trading

## Measure of liquidty

Passive and aggresive sides of a trade. More directly related to broker behavior.
Difficult to measure without persistent broker identification of an unfragmented market
(which we have).

## Dataset

Every trade from the ASX, Australian stock exchange, from 2013. Features:

* Identifiers for the buyer and seller of trades
* Marked with agg/pass
* Relatively unfragmented market -- data captures almost complete picture of trading activity
* 8 Known proprietary HFTs (de-identified) [A-H]

## Removed slides

Lots of fancy graphs I couldn't capture.

## Packages used

* bit64
* data.table
* igraph
* ggplot2
* RColorBrewer
