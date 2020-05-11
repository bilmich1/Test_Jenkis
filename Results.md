## Logz.io

Ressources:  
https://logz.io/blog/jenkins-build-monitoring/  
https://docs.logz.io/shipping/log-sources/jenkins.html  

Pros:  
Good support from Logz.io?

Cons:  
Need to manually build and maintain the logstash-plugin. Logz.io forked the project to add logz.io support, but the plugin isn't up-to-date. The plugin is needed for build logs.

Filebeat for system logs.


## [Jenkins logstash plugin](https://plugins.jenkins.io/logstash/)

Pros:  

Cons:  
The plugins sends each build line as an individual log.

The build time is cummulative by build step. Each build step report the now total time of the build.
We only have the total build time, and not the stages build time, went using `logstashSend` as a post action.
