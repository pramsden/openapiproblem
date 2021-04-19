# openapiproblem

## Goal

To create a multi-module project which uses a single openapi3 description to create a WAR for the REST service, a client which can call the service and a model which can be used wherever the client is used.

## Problem

In eclipse, when `Project->Build Automatically` is selected, the builder goes into an endless loop. In the `Maven Workspace Build` view, all the projects are listed and the `delta` node contains one or more class names.

## The example

This project contains 3 modules: model, client and war. Each uses `openapi-generator-maven-plugin` to generate the required resources. This example is just the bare bones - no further implementation is contained. However, when loaded into eclipse, it should show the endless loop problem.

I originally posted a question on StackOverflow [https://stackoverflow.com/questions/67022024/multi-module-maven-project-builds-continuously-in-eclipse](https://stackoverflow.com/questions/67022024/multi-module-maven-project-builds-continuously-in-eclipse).

Note: I had thought a few times that I had solved the problem but after making small changes the whole thing kicked off again. I have not been able to localise the problem. Also, I have not been able to find a useful description of what the `Maven Workspace Build` view is actually telling me. 
