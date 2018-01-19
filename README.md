# testing
Testing using selenium for phylotastic services

## How to

Using `RSelenium` package to help automate testing: https://cran.r-project.org/web/packages/RSelenium/vignettes/RSelenium-basics.html.

Following instructions on their website, but changing to deal with issues with their listed selenium

```
docker run -d -p 4444:4444 -v /dev/shm:/dev/shm selenium/standalone-chrome:3.8.1-erbium
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
