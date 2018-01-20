# testing
Testing using selenium for phylotastic services

## How to

Using `RSelenium` package to help automate testing: https://cran.r-project.org/web/packages/RSelenium/vignettes/RSelenium-basics.html.

Generally following instructions for RSelenium.  

Make sure you have the right browser driver installed.  Safari apparently doesn't not need a separate driver install, but I was not able to get Safari to work properly, so I switched to Chrome.   

Install chromedriver and put it in your path (see http://www.kenst.com/2015/03/installing-chromedriver-on-mac-osx/)

Start the web driver. 
```
# docker version 
# docker run -d -p 4444:4444 -v /dev/shm:/dev/shm selenium/standalone-chrome:3.8.1-erbium

# run directly with java
java -jar selenium-server-standalone-3.8.1.jar
```

Within R:

```
require(RSelenium)
remDr <- remoteDriver(remoteServerAddr = "localhost", port = 4444L, browserName = "chrome")
remDr$open()
```

This will start the automated browser and report some status details.  

```
remDr$close()
```

