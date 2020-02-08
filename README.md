Suppose we want to predict ridership in Capital Bikeshare for the
current year. The data we've been using so far only covers 2011 and
2012... much too far in the past. Capital Bikeshare has released more
recent ridership data, but it's only ride logs, without the temperature,
holiday, and other helpful features that the [University of
Porto](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset)
data had. And ***they didn't release their code*****...**  

Let's try to wrangle the data ourselves. If we can do that, then we can
easily extend it to more recent data.

The attached notebook has the code you'll need to fetch the raw data to
get started. Your goal is a dataframe that looks like this (showing
every 1000th
row):  


|      | date       | hour | is\_holiday | day\_of\_week | is\_weekend | is\_workingday | temp\_C | rides |
| ---- | ---------- | ---- | ----------- | ------------- | ----------- | -------------- | ------- | ----- |
| 0    | 2011-01-01 | 0    | False       | 5             | True        | False          | 5.60    | 13    |
| 1000 | 2011-02-14 | 12   | False       | 0             | False       | True           | 9.15    | 97    |
| 2000 | 2011-03-29 | 16   | False       | 1             | False       | True           | 8.30    | 119   |
| 3000 | 2011-05-10 | 13   | False       | 1             | False       | True           | 17.20   | 150   |
| 4000 | 2011-06-21 | 7    | False       | 1             | False       | True           | 21.10   | 286   |
| 5000 | 2011-08-01 | 23   | False       | 0             | False       | True           | 28.30   | 81    |
| 6000 | 2011-09-13 | 11   | False       | 1             | False       | True           | 20.00   | 119   |
| 7000 | 2011-10-25 | 5    | False       | 1             | False       | True           | 12.80   | 24    |
| 8000 | 2011-12-05 | 22   | False       | 0             | False       | True           | 12.80   | 93    |


To simplify the problem, consider only rides by Members ("registered" in
the Porto data). (Your table may not match exactly due to legitimate
differences in how to process this data.)  

This is a challenging task. To help break it down, **start by making a
diagram of the process**. At each step, show what the data currently
looks like (relevant column headers, one example row, and a note of what
each row represents). Label the arrows with what operation you'll
perform (in English, not code) to get to the next step.

**Note**: The example solution only has one loop (and even that's not
necessary if you do it in a different order). If you find yourself
wanting to write loops, think instead about how to express the
operations using the "Grammar of Data" we've been discussing (grouping,
querying, joining, ...).  
