---
author: nick
comments: false
date: 2014-01-14 16:51:52+00:00
layout: post
link: http://nickmalleson.co.uk/2014/01/multi-dimensional-kde-test-application-to-geography/
slug: multi-dimensional-kde-test-application-to-geography
title: 'Multi-dimensional KDE test: application to geography?'
wordpress_id: 559
categories:
- mapping / GIS
---

I recently came across this paper in PNAS:



	
  * Doung, T., G. Bruno  and  S. Kristine (2012) Closed-form density-based framework for automatic detection of cellular morphology changes. _PNAS_ [109 (22) pp 8382-8387](http://www.pnas.org/content/109/22/8382.long) (DOI: 10.1073/pnas.1117796109).


The authors describe a kernel density-based multivariate two-sample test. They applied it to study cell biology, but I don't see any reason it couldn't be adapted to compare differences in two spatial point patterns. And it looks like the test can work with data in more than two dimensions, so there is the possibility of including time as well.

Happily, one of the authors ([Tarn Doung](http://www.mvstat.net/tduong/)) has built a package called [ks](http://cran.r-project.org/web/packages/ks/ks.pdf) (kernel smoothing) in R to run the algorithm. The package also contains functions to create kernel density estimates from point data, so I thought I'd give it a go. The data are all reported crimes in London in February and March 2013 available from [data.police.uk](http://data.police.uk/).



<table >
<tbody >
<tr >

<td >T
</td>

<td >0.00
</td>
</tr>
<tr >

<td >z
</td>

<td >1611.302
</td>
</tr>
<tr >

<td >p (two tailed)
</td>

<td >0.0
</td>
</tr>
</tbody>
</table>



The image below shows the crime density for the two data sets (February and March) created using the kde function in R (top) and ArcMap (bottom). I then ran the test itself ([kde.test](http://www.inside-r.org/packages/cran/ks/docs/Hpi.kfe)) to determine the difference in spatial distribution of London crimes in February and March last year. The results are in the right table. The z statistic is the normalised version of T, where higher z values suggest data that are drawn from a different distributions.

Without making another comparison it is hard to know whether the z value is 'high' or not, but as a first step this method looks promising. The code and all data to produce the maps and run the test are available on my git repository: [https://github.com/nickmalleson/KDE_Test](https://github.com/nickmalleson/KDE_Test)

[![KDE Test](http://nickmalleson.co.uk/wp-content/uploads/2014/01/blog_kde_test.png)](http://nickmalleson.co.uk/wp-content/uploads/2014/01/blog_kde_test.png)


