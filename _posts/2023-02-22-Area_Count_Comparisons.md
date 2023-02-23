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


## Paired Poisson Counts 

[ ] Talk to Stephen about this.


## Differences in Differenes

[ ] Talk to Rob about this.



