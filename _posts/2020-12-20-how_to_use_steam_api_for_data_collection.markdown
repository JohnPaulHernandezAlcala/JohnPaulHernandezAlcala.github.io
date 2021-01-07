---
layout: post
title:      "Setting Up a Selenium Bot for Scraping Steam Data"
date:       2020-12-20 23:34:54 -0500
permalink:  how_to_use_steam_api_for_data_collection
---


![Steam](https://assets.vg247.com/current//2018/06/steam-logo1-600x337.jpg)

Interacting with an API can be daunting especially if the documentation is spread between wiki pages like Steam has theirs. When I first performed a Google search on how to use the Steam API, I noticed there were many libraries that had been created to make the process easier. I was so enthralled to discover this, until I realized each one that I tried to use either no longer worked or was not clear with how to use it. 

![Confused gif](https://media.giphy.com/media/glmRyiSI3v5E4/giphy-downsized-large.gif)


Eventually, I learned how to make request to the Steam API! It was actually more simple than I thought initially. Here is how I did it:

```
import json
import requests
# Make Requests to Steam for all applications which include games and DLC's
URL = "https://api.steampowered.com"
data = requests.get(url="https://api.steampowered.com/ISteamApps/GetAppList/v2", ).json()
```

Fast-forward two days, and I realized that game ownership data was recently made unavailable as of 2018 (keep reading for details); that is until I ran across [Steam Spy]( https://steamspy.com/). So I used the Steam API to tell me which appids were actually games and then fed these ids to Steam Spy to get ownership and other data. [Although the data in Steam Spy is not as accurate as it was pre-2018,](https://www.polygon.com/2018/6/30/17521296/valve-steam-spy-replacement-tools-metrics), it is still very valuable because the current data is derived from historical data collected since at the latest 2014. Maybe you ask, why not just ask Steam if they have the better tools available that they promised would be developed soon in 2018. Turns out, they have no real timeline in place:

[Steam Chat](https://drive.google.com/file/d/1nPOJi-ghv9183ElQ5W1YHHtiH7DAgPez/view?usp=sharing)
 
Upon further inspection of Steam Spy, it appears that the creator of Steam Spy, Sergey Galyonkin, has a [Patreon]( https://www.patreon.com/steamspy) account where you can even access more data. The problem is that the provided API does not provide this additional data. Therefore, I concluded that scraping would be my best plan of action. So, after checking the Privacy agreement and the [Robots.txt](https://steamspy.com/robots.txt) of Steam Spy ([What is a robots.txt file](https://moz.com/learn/seo/robotstxt)--click here to find out!), I felt like this was a green light to scrape. With a little help from Selenium’s chrome driver, I set my little scrapping bot to do all my bidding.
Here is how I started my bot:

```
# Sets up a Chrome driver from default profile. NOTE: you cannot use Chrome driver and actively use Chrome at the same time or the code will # not work.
from selenium import webdriver
options = webdriver.ChromeOptions()
options.add_argument(r'user-data-dir=C:\Users\[will be unique to you]\AppData\Local\Google\Chrome\User Data')
# Create chrome driver
driver = webdriver.Chrome(os.getcwd()+"\\chromedriver.exe", options=options)
# Go to game page on Steam Spy
appid = str([put your appid here])
driver.get("https://steamspy.com/app/" + appid)
```

After trial and error, I was able to collect all the data I needed to conduct my analysis into which game features result in high ownership by Steam users. Check it out here: [Steam Game Analysis]( https://github.com/JohnPaulHernandezAlcala/steam-games/blob/main/README.md)

