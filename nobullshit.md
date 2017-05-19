# No Bullshit Data Science

by Szilard Pafka.

## Big data is bullshit

It is.

"The only way is buy 100 servers, rent it on amazon in the cloud,
install Hadoop or Spark. The only way to deal with such amounts of 
data!"

Szilard says f that. 

Most "big data" tools are hard to use.

"It takes a big man to admit his data is small" - Hadley Wickhan @jcheng
"It's not always the size that matters ;)" - Szilard Pafka

EC2 machine go up to 2TB RAM. You will be fine lol.

## Repos

* [szilard/benchm-databases](https://github.com/szilard/benchm-databases)
* [szilard/benchm-ml](https://github.com/szilard/benchm-ml)
* [szilard/dataset-sizes-kdnuggets](https://github.com/szilard/dataset-sizes-kdnuggets)

Check out [Szilard's github](https://github.com/szilard).

"data.table is one of the fastest things for any kind of aggregation and joins with."

## Summary / tips

* Get lots of RAM physical / cloud
* Use R/Py and high perf pkgs (data.table, xgb)
* Do data reduction in db
* Missed last 4

## Example 2

Which open source tools off the shelf can we use to do binary classification
on 10 million records?

“I really use other people’s code. I can find open source code for what I want to do , and my time is much better spent doing research and feature engineering.” - Owen Zhang

See the github repo:

* [szilard/benchm-ml](https://github.com/szilard/benchm-ml)

Algorithms considered were

* BST-DT
* RF
* BAG-DT
* SVM
* ANN
* KNN
* BST-STMP
* DT
* LOGREG
* NB

See the cornell paper.

## For winning Kaggle

Use all of the above and clever tuning and stacking.

* R pkgs
* Python scitki-learn
* Vowpal wabbit
* h2o
* xgboost
* spark mllib
* a few commercial ones

These all promise you everything:

* lightning fast
* big data
* large scale
* optimized
* distributed
* scalable and fast

