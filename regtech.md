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

##  Notes on figures

These went really quick so hard to get detailed notes.

Close to 11% are forwarded without any text. These are excluded.

Plot.
Fig 1. Avg email length over time.
Year 2000 vs 2001.

Email lenght was stable at 400 characters per email mean but then as
market declined **email length spiked upward**. Then when market went south
**email lenght went way way down** ("come see me" etc)

Fig 2. Email sentiment and disagreement over time

Fig 3. Factiva News Coverage over Time
Weekly Time Series Plot of Articles Published

Fig 4. Missed

Fig 5. Stock Returns and Net Sentiment over time

* Net sentiment across enron employee emails over time
* Moving avg stock returns for enron over time

Downward trend across both plots.

Fig 6. Stock prices and net sentiment over time

Fig 7. Stock returns & email length over time

* moving avg email length across all employees
* moving avg stock returns for enron over time

