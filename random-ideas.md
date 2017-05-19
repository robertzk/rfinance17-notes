# Random ideas for connecting syberia with trading

## HFT

To use Syberia for HFT, here's one idea.

* Define a backtesting engine and grammar
* Use it to visualize and test a variety of trading strategies in R
* Define Syberia resources to transpile backtesting strategy from R to VHDL
* Push directly to FGPA array and trade on the wire

In this vision, one team of quants and traders is identifying
optimal trading strategies, and a separate team of "trading data engineers,"
i.e., low-level distribution systems developers are
defining the transpilation layer that creates custom FPGAs
to execute the trading strategies in microseconds.
