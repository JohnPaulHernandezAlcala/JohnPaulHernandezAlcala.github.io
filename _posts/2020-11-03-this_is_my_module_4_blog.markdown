---
layout: post
title:      "Neural Network Madness: Quick Overview and Excellent Resource"
date:       2020-11-03 18:53:39 -0500
permalink:  this_is_my_module_4_blog
---


It seems like technical news is always talking about how neural network models are helping predict this or detect that. For example, a recent article came out describing how [MIT researchers have developed a model that can identify 97% of COVID-19 just by a person’s cough—even in asymptomatic people](https://www.sciencealert.com/ai-cough-analysis-could-detect-covid-19-even-if-you-re-asymptomatic). When you first hear it without any background, immediately, it sounds like something that is way beyond what you can comprehend. Why? Because it sounds like it has something to do with the brain and that sounds complicated.

However, when you take the time to slowly digest this model, you realize that it is made up of very familiar parts. Check out his video series for great visuals: https://www.youtube.com/watch?v=CqOfi41LfDw&ab_channel=StatQuestwithJoshStarmer

Basically, we see how a input values are transformed by being fed into a fit line-like equation (e.g. x value for y=slope*x+y_0) with a previously obtained weight (slope) and y-intercept (bias) in; the results are the x-values of the activation function you select such as RELU or softplus. We input these x-values into the activation function to find the corresponding y-values. At this point, we are in a hidden layer. Thereafter, these output hidden node values are scaled by a certain weight, added to each other according to neural network organization, and modified (addition) by another bias value. The output values from all this is the output layer. That is it! The more complicated Neural Networks are just layers of this same concept.



Maybe you are curious how we get those previously obtained weight and bias values. It is more involved, but it is essentially the same steps but with equations.

If all of this sounds confusing, please check out the video referenced above because it has great visuals!

