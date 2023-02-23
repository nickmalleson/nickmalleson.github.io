---
layout: post
title: "Comparing Event Counts in Neighbourhoods"
tagline:
category: announce
tags: [GISc]
---

# Approaches to Identifying Statistically-Significant Differences in Area-Based Event Counts

I recently asked my research group, [CSAP](https://environment.leeds.ac.uk/geography-research-centre-spatial-analysis-policy), what peoples' go-to methods for estimating whether a change in the number (or proportion) of events in a neighbourhood is statistically significant. 

For example, if Area A has 2% of all events in one year and 4% of all events in another year, is that a significant difference?

I received some interesting and diverse answers:

## Standard Error of a Proportion

Convert the event counts into proportions (or percentages) and then calculate the standard error (SE) of the proportions for each area.
These standard errors can the be used to measure the (95%) confidence interval around the proportions for each area.
If the confidence intervals for two areas overlap then you cannot be confident that the difference is significant. 

The SE is calculated as follows:
$$
  SE = \sqrt{ \frac{p(1-p)}{n}}
$$
where $p$ is the proprtion of events in an area and $n$ is the denominator for that area. 
The 95% confidence interval (CI) is then:
$$
  CI = 1.96 \pm SE
$$

[This website](https://online.stat.psu.edu/stat100/lesson/9/9.3) mentions that approach (at the bottom of example 9.6). 

Another similar approach is to calculate a confidence interval for the _difference_ in population proportions. If the confidence interval does not contain 0 then it is likely that there is a 'true' difference in the two proportions. [This website](https://www.statology.org/confidence-interval-difference-in-proportions/) has a good worked example. 

## Confidence Interval around the Mean Distance

This method looks at the difference itself, rather than the distrubtions of the events. 
In short, for each area you calculate the difference in the number of events and then calculate the z-scores for the difference. Any area with a difference of $z>x$ (i.e. where $x=2$ you are identifying areas with a difference that is 2 standard deviations above the mean) could be statistically significant. The following R code helpfully shows this (thanks Lex!).

```R
# Make some data with poisson distibution (counts)
# I would suggest that these could be convereted to rates with something per 1000 people / hopuses etc
# BUT because you have 2 of them they should approximate to a normal distributiuon when compared

events_yr1 = rpois(500, lambda = 3)
events_yr2 = rpois(500, lambda = 3)
# calculate difference - shoudl have a normal-ish distribution
dif = events_yr1-events_yr2
hist(dif)
# now z-scores
dif_z = as.vector(scale(dif))
hist(dif_z)

# now find signioficant changes
# combine to a df
df = data.frame(e1 = events_yr1, e2 = events_yr2, dif = dif, dif_z = dif_z)
head(df)
big_change = which(df$dif_z > 2 | df$dif_z < -2)
big_change
df[big_change, ]
```


## Paired Poisson Counts 

[ ] Talk to Stephen about this.


## Differences in Differenes

[ ] Talk to Rob about this.



