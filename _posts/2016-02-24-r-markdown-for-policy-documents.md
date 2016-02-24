---
layout: page
title:  Reproducible policy documents in R
date: 2016-02-24 00:57:09
published: true
tags: [example1, example2]
feature-img: "images/policy_doc.png"
---


Reproducible documents in R markdown have focused on science and technical data. Along with distributed version control, the R package system, unit testing and continuous integration resources there is a suite of tools which were original developed for collaborating and testing code and digital resouces which now are being used more widely for all types of documentation and processes in science and beyond.

Got me wondering how far this could be taken. Even though there's plenty of technical aspects in terms of how best to use and collaborate using these types of documents, particularly between the non-technical end-user and the coder. There's some really interesting work outlined in this [paper](https://www.stat.auckland.ac.nz/~paul/Reports/invert/invert.html) on ways this can be done.

I'd been thinking about if Rmarkdown could be used in policy or legal documents. These documents are have a very complicated structure which can make a even your most convoluted git repository look like a minimalist masterpiece in comparison. And it (seems git version control)[https://legixinfo.wordpress.com/2015/08/12/can-github-be-used-to-manage-legislation/] isn't necessarily a solution for legal documents.  The structure of legal documents has also been formalised in a number of ways within the UK and else where for instance there are [xml formats](http://www.legislation.gov.uk/developer/formats) as well as a more broad [international xml standard](http://www.akomantoso.org/). Some interesting tools for editing and updating laws are also being development. So aside from the xml formatting and issues around versioning - is there a place for Rmarkdown?
 
I think R markdown documents, particularly for policy could be a building block for the services and reports that a particular policy outlines. Making the text of a legal document the foundation of a data dictionary and web service which delivers the outcomes, measures the performance, creates the reports and ultimately provides feedback as to whether the policy is successful or not. This document would also be easy to transferable/adjustable for different jurisdiction.

So I've drafted, the first piece of Rmarkdown legislation. It's early days, but I've uploaded an R package to github for cloning called [Policy](https://github.com/fozy81/policy). It's apolicy to reduce street litter. You can change the area parameter value when rendering (see details of how this can be done in rstudio [here](http://rmarkdown.rstudio.com/developer_parameterized_reports.html)). 

If the area name you enter matches an admin area in OpenStreetMap (admin_level = 6) i.e. roughly equal to county/council jurisdiction, it will download the road network from openstreetmap, work out how much distance that covers, sets up surveying points to create a baseline survey to record the amount of litter present and displays a simple map. Once the data on the amount of litter is collect, is could be the basis of a shiny app...the level of fines for litter could be adjusted and the outcomes of different levels of fine compared. The fines could be automatically adjusted for inflation. 

![doc_map]({{ site.url }}images/policy_map.png)




