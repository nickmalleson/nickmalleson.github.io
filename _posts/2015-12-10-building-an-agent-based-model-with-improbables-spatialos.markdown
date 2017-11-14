---
author: nick
comments: false
date: 2015-12-10 10:18:09+00:00
layout: post
link: http://nickmalleson.co.uk/2015/12/building-an-agent-based-model-with-improbables-spatialos/
slug: building-an-agent-based-model-with-improbables-spatialos
title: Building an Agent-Based Model with Improbable’s SpatialOS
wordpress_id: 863
categories:
- agent-based modelling
---


<figure class="right">
  <img src="{{site.url}}/{{site.baseurl}}/wp-content/uploads/2015/12/spatialOS-300x174.png" />
  <figcaption>A diagram of Spatial OS (<a href="http://improbable.io/learn-more">source</a>).</figcaption>
</figure>

I recently spent a week working with [improbable](http://improbable.io/), a tech startup in London. Improbable are in the process of creating a simulation engine called [SpatialOS](http://improbable.io/learn-more). Basically, the idea is to create a platform that researchers/developers/etc. can use to simulate massive systems that have large numbers of interacting units. The thing that is particularly nice about SpatialOS is that it seamlessly splits up a large model into smaller chunks, and distributes these chunks to different cores, or different computers across a network. This will make it possible to simulate huge systems, like cities, by spreading the work over a number of different computers in the cloud.

The software is still under development, but it's easy to use. After a couple of days I had learned the basics and was able to implement a simple agent-based model of people commuting in Leeds (see the video below). The model reads in information about the number of people who live in each Lower Super Output Area in Leeds (LSOAs are a neighbourhood boundary used for the census and other administrative things) and where they commute to. It has a 24-hour clock and the individual agents go to work in the morning, coming home again in the afternoon. At the moment it only simulates 1,350 agents, but when the model is scaled-up on a larger computer system it should be possible to model to the 750,000 people in the city.



<iframe width="560" height="315" src="https://www.youtube.com/embed/f2TqsVr7IzU" frameborder="0" allowfullscreen></iframe>


Another nice feature of the software is that it has been integrated with the [Unity](https://unity3d.com/) game engine. This provides a good 3D interface to view a running model, and also provides access to advanced features like physics models that are usually beyond the capabilities of most modellers. The video above shows the model running with Unity as the front-end.

On the whole it's very exciting, and I'm looking forward to continuing to develop my agent-based model of urban flows with it.
