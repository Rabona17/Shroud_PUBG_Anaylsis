# Shroud_PUBG_Anaylsis
This was my first project working on data-gathering and analysis. The project was done on Oct, 2018.

I web-scrapped the official site of PUBG to get most 1600 recent duo games of the famous streamer Shroud, and I make simple analysis on them using Pandas
## Original website
[The Official PUBG website](https://pubg.op.gg/user/shroud?server=na&hl=en) provides these data. Note that this website is a dynamic website using `Ajax`, the major two ways to scrape the whole data is to use webdriver like `Selenium` or find the api and the Json format of the data. Here I found the api to the data and it looks like [this](https://pubg.op.gg/api/users/59fe237a6e6f210001da80f9/matches/recent?after=eyJfaWQiOiI1YzU1NGQ1YzU4N2Y2YzAyMDk3M2QyMzIiLCJzdGFydGVkX2F0IjoxNTQ5MDcwNzg1LCJzZWFzb24iOiJwYy0yMDE4LTAyIn0%3D).

The api is comprised of several key words. After analzing, I found that to get more and more data, the text after `after=` should be changed to any `ID` of a game so that it will show 20 more match data that is after the match that the `ID` represent.
## Techniques involved
* Web-Scraping using `Beautifulsoup` and `Json`.
* Data Cleaning using `Numpy` and `Pandas`.
* Simple `time-series` analysis and data visualization using `Matplotlib`.
