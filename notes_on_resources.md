
This is information mainly from Arlin's colleague Casey, with a few bits contributed by Matt Yoder. 

## Cucumber 

* https://cucumber.io 
* a list of available docs (including instructions) is https://cucumber.io/docs
* Cucumber is actually the framework, the language is Gherkin: https://github.com/cucumber/cucumber/wiki/Gherkin

For a fun way to experiment, here’s a minimal version that can be installed with Node.js
https://github.com/cucumber/microcuke

## Browser automation

* Selenium - browser functional tests

## Some various monitoring tools:

* Nagios: https://www.nagios.com/solutions/website-monitoring/ This is the go-to.
* Zabbix: http://www.zabbix.com/ This is one we’ve installed on a few servers here.

I have heard of OpenNMS, but confess that’s about as far as my knowledge of it goes:
* https://www.opennms.org/en

And I’ve never heard of either Icenga or Sensu until today, but in some ways they may be other options as well. Sensu seems to be good at monitoring and notification, but I didn’t see capabilities to fire simple scripts.
* Icenga: https://www.icinga.org/products/icinga-2/features/ reportedly an offshoot of Nagios trying to rebuild better.
* Sensu: https://sensuapp.org/features

## Continuous integration
There are also continuous integration (CI) tools which perform the act of building and running unit tests immediately upon any commit. This can also take the place of using something like cucumber, but can entail a larger learning curve. Examples of these might be
* Jenkins https://jenkins.io/
* TravisCI: https://travis-ci.org/ or https://travis-ci.com/

In the latter case, you can implement TravisCI for any GitHub project, public or private, by registering with TravisCI, and placing a .travis.yml file which configures the build steps into your root.

Matt adds: 
* CircleCI alternative to TravisCI, with higher learning curve but ability to SSH into test build
