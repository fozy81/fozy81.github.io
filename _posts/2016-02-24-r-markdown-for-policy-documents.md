---
layout: post
title:  Reproducible policy documents in R
date: 2016-02-25 21:39:20
published: true
tags: [rmarkdown, rstats, policy]
---

Reproducible documents in Rmarkdown have focused on science and technical data. Along with distributed version control, the R package system, unit testing and continuous integration resources there is a suite of tools which were originally developed for collaborating and testing code but now are being used more widely for all types of documentation and processes in science and beyond.

Got me wondering how far this could be taken. Even though there's plenty of technical challenges in terms of how best to use and collaborate using these types of documents, particularly between the non-technical end-user and the coder. There's some really interesting work outlined in this [paper](https://www.stat.auckland.ac.nz/~paul/Reports/invert/invert.html) on ways this can be done.

I'd been thinking about if Rmarkdown could be used in policy or legal documents. These documents generally have very complicated structures which can make even your most convoluted git repository look like a minimalist masterpiece. And it [seems git version control](https://legixinfo.wordpress.com/2015/08/12/can-github-be-used-to-manage-legislation/) isn't necessarily a solution for legal documents. The structure of legal documents has also been formalised in a number of ways within the UK and elsewhere for instance there are [xml formats](http://www.legislation.gov.uk/developer/formats) as well as a more broad [international xml standard](http://www.akomantoso.org/). Some interesting tools for editing and updating laws are also being development. So aside from the xml formatting and issues around versioning - is there a place for Rmarkdown?
 
Maybe an Rmarkdown policy doc for reducing litter?

![policy doc]({{ site.url }}/images/policy_doc.png)
 
I think R markdown documents, particularly for policy could be a building block for the services and reports that a particular policy outlines. Making the text of a legal document the foundation of a data dictionary and web service which delivers the outcomes, measures the performance, creates the reports and ultimately provides feedback as to whether the policy is successful or not. This document would also be easy to transfer/adjust for different jurisdiction.

So I've drafted, the first piece of Rmarkdown legislation. It's early days, but I've uploaded an R package to github for cloning called [Policy](https://github.com/fozy81/policy). It's a policy to reduce street litter. You can change the area parameter value when rendering (see details of how this can be done in rstudio [here](http://rmarkdown.rstudio.com/developer_parameterized_reports.html) ). 
 
If the area name you enter matches an admin area in OpenStreetMap (admin_level = 6) i.e. roughly equal to county/council jurisdiction, it will download the road network from openstreetmap, work out how much distance that covers, sets up surveying points to create a baseline survey to record the amount of litter present and displays a simple map.

![doc_map]({{ site.url }}/images/policy_map.png)

Once the data on the amount of litter is collect, this data could be the basis of a shiny app...the level of fines for littering could be adjusted and the outcomes of different levels of fine compared. The fines could be automatically adjusted for inflation...reports sent out to local councillors...awards for best performing areas...all flowing and linked back to the original document without discrepancies in language, dates, targets.

Just a thought.


