---
title: "R-Opitools – An Opinion Analytical Tool for Big Digital Text Document (DTD)"
date: "30th July 2021"
bibliography: paper.bib
output: pdf_document
affiliations:
- name: Crime and Well-being Big Data Centre, Manchester Metropolitan University
  index: 1
tags:
- digital text document
- sentiment analysis
- opinion mining
- randomization testing
authors:
- name: Monsuru Adepeju
  orcid: 0000-0002-9006-4934
  affiliation: 1
---

# Statement of Need

Since the year 2000, various computational intelligence techniques have been developed for analyzing sentiments of users either in the field of natural language processing or computational linguistics. To date, the majority of the techniques as deployed across various fields, including Social science [@Somasundaran:2010; @Morency:2011; @Nikolovska:2020], Market research [@Feldman:2011; @Otaibi:2018], and Electoral politics [@Ansari:2020; @Connor:2010] have focused largely on detecting subjectivity, and/or extracting and classifying sentiments and opinions in a text document. Building on this existing work, the current paper advances an opinion impact analytical tool, namely; `Opitools`, that does not only extracts inherent themes from within a digital text document (DTD), but also evaluates the extent to which a specified theme may have contributed to the overall opinions expressed by the document. Based on this advancement, `Opitools` holds prospect for wider applications, compared to the existing techniques, in the aforementioned application fields. For example, in Law enforcement, the package can be deployed to understand factors (themes) that drive public perception of the police services [@Adepeju:2021]; in Market research, to identify factors that underlie customers satisfaction in a product; and, in Electoral politics, to identify factors that may be influencing electoral interests in an upcoming election. These examples have also been demonstrated in the documentation of the package (please see the `README.md` file and the package `Vignette` for details). Lastly, it is argued that this contribution provides a framework by which some of the existing opinion mining tools [@Tai:2015; @Kiomourtzis:2014; @Wawer:2016; @Munson:2019] may be further advanced for wider research impacts.

# Implementation

Having extracted a set of thematic keywords from a digital text document, the goal is to computationally classify the sentiments expressed in each text record into positive, negative or a neutral sentiment, using a lexicon-based classification approach [@Nielsen:2011; @Adepeju:2021]. The resulting sentiment scores are combined in order to estimate the overall opinion score of the document. To assess the impacts of a selected theme (or a subject) on the estimated opinion score, we simply ask the question; *If expected opinion scores were generated under the null hypothesis, how likely would we be to find a score higher than the estimated score?*. The question is answered by employing a non-parametric randomization testing strategy [@Fisher:1935; @Good:2006] which involves random re-assignment of sentiment labels of the original text document to derive the expectation distribution, which is then compared with the observed score to obtain the statistical significance of the impacts.


# Key Functionalities

The package contains text exploratory functions, including `opi_imp`,  for extracting themes from a digital text document. To conduct the impact analysis, the `opi_impact()` function draws from two supporting functions, `opi_score()` and `opi_sim()`, to compute the observed opinion score and its expectations, respectively. 

Different types of opinion score functions are embedded in the package for user-selection based on the research question been investigated. A `'fun'` parameter is also included to allow the integration of pre-defined user score functions. This feature is to further facilitate the uptake of the package in more application fields.

# Acknowledgment

We gratefully acknowledge the Economic and Social Research Council (ESRC), who funded the Understanding Inequalities project (Grant Reference ES/P009301/1) through which this research was conducted.

# References

