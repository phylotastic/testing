# testing
Testing using selenium for phylotastic services

## How to

Using `RSelenium` package to help automate testing: https://cran.r-project.org/web/packages/RSelenium/vignettes/RSelenium-basics.html.

Following instructions on their website:

```
docker run -d -p 5901:5900 -p 127.0.0.1:4445:4444 --link http-server selenium/standalone-firefox-debug:2.53.1
```

Within R:

```
require(RSelenium)
remDr <- remoteDriver(remoteServerAddr = "localhost"
                      , port = 4445L
                      , browserName = "firefox"
                      )
remDr$open()
```
