# How to change log level in Springboot applications runtime

## Intro
This simple example shows how easy it is to change log level while your applications is running so it saves you the hassle of restart it just to change to DEBUG or TRACE.


## Building
This is a gradle project. Just run the following command to build the project:
``gradle clean build``


## Endpoints and Demonstration
* __GET:__ localhost:8080/ping
* __POST:__ localhost:8080/loglevel/{loglevel}?package={package-name}


After starting the application (INFO being the default log level) we want to change this to DEBUG on the only package avaiable:

``curl -XPOST localhost:8080/loglevel/debug?package=se.roger``

We can then verify that we are getting DEBUG logging by hitting the ping endpoint:

``curl -XGET localhost:8080/ping```
