---
author: nick
comments: false
date: 2014-02-18 20:48:58+00:00
layout: post
link: http://nickmalleson.co.uk/2014/02/uk-government-spending-treemap/
slug: uk-government-spending-treemap
title: UK Government Spending Treemap
wordpress_id: 579
categories:
- visualisation
---

Inspired by David McCandless' TED talk ([the beauty of data visualization](http://www.ted.com/talks/david_mccandless_the_beauty_of_data_visualization.html)), I decided to try to visualise government spending in a useful way. This is particularly relevant given the current worry over state spending on benefits. Happily the Guardian have collected all the [data](http://www.theguardian.com/news/datablog/2012/dec/04/government-spending-department-2011-12), otherwise this would probably have been impossible (given the amount of time I wanted to spend on it).

In the visualisation below the budgets of different departments have been sub-divided into different spending categories. There are no real surprises, but I found it interesting how small the budgets of departments like Ministry of Justice and Department for Transport were when compared to the Department of Work & Pensions and the Department of Health. Also, spending on the state pension vastly outweighs other DWP spending on things like housing benefit.


[![UK government spending treemap](https://raw.github.com/nickmalleson/Govt_Spending/master/code/figure/treemap2.png)](https://github.com/nickmalleson/Govt_Spending)




The visualisation was created using the treemap package in R. Code and data are both available publicly on github: [https://github.com/nickmalleson/Govt_Spending ](https://github.com/nickmalleson/Govt_Spending)
