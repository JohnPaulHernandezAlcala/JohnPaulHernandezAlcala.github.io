---
layout: post
title:      "How to Use Steam API for Data Collection"
date:       2020-12-21 04:34:53 +0000
permalink:  how_to_use_steam_api_for_data_collection
---

![Steam](https://assets.vg247.com/current//2018/06/steam-logo1-600x337.jpg)
Interacting with an API can be daunting especially if the documentation is spread between wiki pages like Steam has theirs. When I first performed a Google search on how to use the Steam API, I noticed there were many libraries that had been created to make the process easier. I was so enthralled to discover this, until I realized each one that I tried to use either no longer worked or was not clear with how to use it. 
Confused gif
Fast-forward two days, and I realized I was not getting anywhere. That is until I ran across [Steam Spy]( https://steamspy.com/). From here, I relearned how to make basic requests with the provided Steam Spy API that pulled information from the Steam API. [Although the data in Steam Spy is not as accurate as it was pre-2018,](https://www.polygon.com/2018/6/30/17521296/valve-steam-spy-replacement-tools-metrics), it is still very valuable because of the current data is derived from historical data collected since 2014. Maybe you ask, why not just ask Steam if they have the better tools available that they promised would be developed soon in 2018. Turns out, they have no real timeline in place:
 

So, the only real data that is available is through Steam Spy. Here is the API address for making requests through: http://steamspy.com/api.php
Just in case you need a refresher how to make requests, I will present below how to make a request to the above API address

Upon further inspection of Steam Spy, it appears that the creator of Steam Spy, Sergey Galyonkin, has a [Patreon]( https://www.patreon.com/steamspy) account where you can even access more data. The problem is that the provided API does not provide this additional data. Therefore, I concluded that scraping would be my best plan of action. So, after checking the Privacy agreement and the [Robots.txt](https://steamspy.com/robots.txt) of Steam Spy ([What is a robots.txt file](https://moz.com/learn/seo/robotstxt)--click here to find out!), I felt like this was a green light to scrape. Unfortunately, the Steam data holy grail is behind two guardians: Login and reCaptcha.
(gif guards)[]

