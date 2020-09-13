---
layout: post
title:      "This is the title for my module 3 project blog"
date:       2020-08-28 19:27:28 -0400
permalink:  this_is_the_title_for_my_module_3_project_blog
---


After completing my [third project]( https://github.com/JohnPaulHernandezAlcala/Bank-Targeted-Marketing), I have learned a lot about training different models with my processed data, using those models to make predictions, and evaluating their performance; however, what I failed to fully grasp is how some of these models were actually doing all these amazing calculations in the background. So, I decided to do further investigation into 3 of the models without going too deeply into the math—after all, this is were most of us tend to get lost.

Logistic Regression: 
![]( https://miro.medium.com/max/1428/1*Vd9ZTC1zWJPtV7iXPMJk1Q.png)

“Used when data is binary (two classes). Classifies data in one group versus another one; this model will assign a ‘probability’ of belonging to one group versus another one.”

When I read the above, it did not make a ton of sense, but after I looked up some other resources, I learned that it is similar to linear regression, except for it classifies data points in one or another class using probabilities. Instead of using residuals, it uses maximum likelihood, or where the data points are more likely to follow the s-shaped line. Unlike linear regression, logistic regression can use continuous or discrete data like categories for the x-axis, but it can only use two classes for the y-axis.

This this video for good interactive visual: https://www.youtube.com/watch?v=yIYKR4sgzI8&ab_channel=StatQuestwithJoshStarmer

Vector Support Machine:
![]( https://i.imgur.com/WuxyO.png)
“A type of classifier which modifies the loss function for optimization to not only take into account overall accuracy metrics of the resulting predictions, but also to maximize the decision boundary between the data points. In essence, this further helps tune the classifier as a good balance between underfitting and overfitting. Another way of putting it is that it performs classification by finding the separation line or (in higher dimensions) "hyperplane" that maximizes the distance between two classes.”

Hyper-what? The only think I took out of this is that it is able to achieve a good balance between underfitting and overfitting which doesn’t give a lot of detail how. Understanding this took some time before I came across a really good resource that explained it simply. Basically, this model projects the data’s different features into a higher dimensional space to find a easier way to classify the data point. What does this mean? It means for example, if one of your features is weight, that value would be squared

