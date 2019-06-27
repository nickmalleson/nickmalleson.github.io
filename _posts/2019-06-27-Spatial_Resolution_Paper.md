---
layout: post
title: "Spatial Resolution Crime Paper"
tagline: ""
category: announce
tags: [paper, crime, gis]
---

# New Paper: Identifying the appropriate spatial resolution for the analysis of crime patterns

<figure style="float:right; width:50%;" >
<img src="{{site.baseurl}}/figures/paper_figures/msea_2018/msea_method.png" alt="Diagram of the MSEA method"/>
</figure>

Malleson N, Steenbeek W, Andresen MA (2019) Identifying the appropriate spatial resolution for the analysis of crime patterns. _PLoS ONE_ 14(6): e0218324. DOI: [10.1371/journal.pone.0218324](https://doi.org/10.1371/journal.pone.0218324) (open access).

**Background**

A key issue in the analysis of many spatial processes is the choice of an appropriate scale for the analysis. Smaller geographical units are generally preferable for the study of human phenomena because they are less likely to cause heterogeneous groups to be conflated. However, it can be harder to obtain data for small units and small-number problems can frustrate quantitative analysis. This research presents a new approach that can be used to estimate the most appropriate scale at which to aggregate point data to areas.

<figure style="float:left; width:50%;" >
<img src="{{site.baseurl}}/figures/paper_figures/msea_2018/crime_resolution_map.png" alt="Crime density at different resolutions"/>
</figure>

**Data and methods**

The proposed method works by creating a number of regular grids with iteratively smaller cell sizes (increasing grid resolution) and estimating the similarity between two realisations of the point pattern at each resolution. The method is applied first to simulated point patterns and then to real publicly available crime data from the city of Vancouver, Canada. The crime types tested are residential burglary, commercial burglary, theft from vehicle and theft of bike.



**Findings**

The results provide evidence for the size of spatial unit that is the most appropriate for the different types of crime studied. Importantly, the results are dependent on both the number of events in the data and the degree of spatial clustering, so a single ‘appropriate’ scale is not identified. The method is nevertheless useful as a means of better estimating what spatial scale might be appropriate for a particular piece of analysis.
