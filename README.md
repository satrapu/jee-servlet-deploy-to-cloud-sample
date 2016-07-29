jee-deploy-to-cloud
=

Description
--
This application was written in order to experiment with the ways a JEE web application must be configured to successfully deploy it to various (free) cloud providers like Heroku or OpenShift.
This repo contains a very simple JEE 7 servlet which will display some request related information.

Continuous Integration
--
* drone.io: [![Build Status](https://drone.io/github.com/satrapu/jee-deploy-to-cloud/status.png)](https://drone.io/github.com/satrapu/jee-deploy-to-cloud/latest)

Deployment
--
~~This application is deployed to different cloud providers using [wercker] (http://wercker.com/). This tool currently supports~~ ~~deploying applications to Heroku and OpenShift.~~ <b>Currently, wercker is not correctly setup, but I plan on fixing it ... sometime.</b>
<br/>
<br/>
This application is deployed to different cloud providers using their native support.
<br/>
* Heroku - supports, among other deployment options, git deployment; each time you want your local changes from master branch to be deployed to OpenShift, use:
```bash
git push heroku master
```
* OpenShift - supports, among other deployment options, git deployment; each time you want your local changes from master branch to be deployed to OpenShift, use:
```bash
git push openshift master
```

Live Application
--
* ~~Heroku: https://jee-deploy-to-cloud.herokuapp.com/status~~ Currently, it's incorrectly configured, but I plan on fixing it soon by deploying an uberjar built via [WildFly Swarm](http://wildfly-swarm.io/) and starting a Heroky web dyno with "java -jar ...-swarm.jar"
* OpenShift: http://jee-satrapu.rhcloud.com/status/
