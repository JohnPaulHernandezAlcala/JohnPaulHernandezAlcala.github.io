---
layout: post
title:      "Data's Basic Story Telling Tools: Bar Graph and Histogram Graph"
date:       2020-04-07 02:40:21 +0000
permalink:  datas_basic_story_telling_tools_bar_graph_and_histogram_graph
---


The content of your blog post goes here.Most of the problems that data scientists must solve involve how much or how many? (regression), which category? (classification), what’s wrong with the data? (anomaly detection), and would a user prefer this? (recommender systems). The first step to solving any of these problems is to determine what type of data is at hand. So, if I am asked to compare the number of companies with their associated revenues, which graph would I use? 

A bar graph because I am comparing different companies, right? Not exactly. Let’s talk about it. Bar graphs allow comparisons across categories by presenting categorical data as bars with heights proportional to the values that they represent such as revenue. Additionally, the order of these categories does not matter, so the bars are labelled as companies and can be in any order. A histogram is a plot that lets you discover the underlying frequency distribution of a data set and allows you to visualize fundamental properties about the data such as if it is skewed in any particular direction (positively or negatively) or if it has outliers that need additional processing (elimination or inclusion). So, the bars are not labelled by company name but are bins for companies to go into and each of these bins has a certain number of companies going into it which is frequency.

More specifically, in contrast to bar graph’s bars, the bars in a histogram represent ranged values for the data. Furthermore, histograms can also be used as an additional aid to help decide between different measures of central tendency such as mean, median, and mode for data representation or how best to answer my question.

So, it is important to distinguish bar graphs from histograms because depending on the data being analyzed (in our case the number of companies) it makes conclusions easier and clearer. Bar graphs show category-specific values and consist of two variables. So, if the original question wanted us to compare total revenue between all the companies, then a bar graph would be the appropriate choice. Histograms show counts of how frequently a given range of values occurs in a data set. So, our original question is telling us to use a histogram because it asked to compare the “number of companies” (i.e. bins) on a revenue range. When you view a histogram, you can always visually locate the bin where most of the values occur (as peaks). That is the concept that a measure of central tendency attempts to represent as a number. By simply changing the bin size, it allows better comprehension of the distribution of underlying data. 

In summary, if the data sounds like it involves just categorical comparison (e.g. company names) and no ranges, then a bar graph is the right choice over histogram; conversely, if the data sounds like it involves ranges, then histogram graph is the right choice. When we know what the data is telling us it needs, we are allowing it to tell its full story with clarity and succinctness.

