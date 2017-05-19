# Reg Tech

Seoyoung Kim: Zero-Revelation RegTech: Detecting Risk through Linguistic Analysis of Corporate Emails and News

Financials are delayed indicators of corporate quality.

Internal discussion may be used as an early warning system.

Automated platform for parsing emails and producing summary stats would be highly valuable since

* it can analyze vast quantities of textual data not amenable to human processing
* does not require revelation of individual email content explicitly to monitor

## Purpose

Explore predictive power of employee emails. Can do:

* Sentiment analysis.
* Information conveyed by structural characteristics e.g. volume of email or length.
* Other non-verbal indicators (shifting email network patterns, etc.)

## Preview of results

* Net sentiment conveyed by Enron employee email is a signicant predictor of stock-return perf
* Email length stronger predictor of price decline than net sentiment
* Try identify other potential indicators / predictors of escalating risk or malfeasance

## Enron corpus

Initial sample:

* Approx 500,000 emails
* Jan 2000 - Dec 2001
* First made public by FERC during investiguation
* Carnegie Mellon CALO project

Caveats:

* Scrubbed for legal reasons to honor reqs from affeted employees
* User fastow-a is missing
* Email chatter surrounding Mr Skilling's sudden resig on 8/14/2001 has been expunged
* Details regarding exclusion criteria are not public. So analys is exploratory and prescriptive

## Curing the data

Focus on sent:

* Analyze content written by enron employees
* Avoid processing same content twice
* User lay-k sends email to skilling-j

Other filters:

* Emails greater than 3000 chars in length
* Emails sent to more than 20 recipients
* News articles from Factiva PR
* Sentiment dics from Harvard inquirer and Loghran and McDonald sentiment word list

## Final sample

* Enron email corpus from CM CS site
* 113266 sent emails
* 114 employees

##  Notes

Close to 11% are forwarded without any text. These are excluded.

Plot.
Fig 1. Avg email length over time.
Year 2000 vs 2001.

