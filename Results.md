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
Very versatile, could allow us to easily add information to the stash

Cons:  
The plugins sends each build line as an individual log.

Needs to indiviually wrap the information we want in an easily tokenizable log entry.

The build time is cummulative by build step. Each build step report the now total time of the build.
We only have the total build time, and not the stages build time went using `logstashSend` as a post action.


## [Jenkins Job and Stage Monitoring plugin + graphana](https://plugins.jenkins.io/github-autostatus/)

Pros:
Very simple to setup visualization

Should support Global build time, stages build time, test reporting (coverage/Test Cases/etc...)

Could allow us to see the stage build time in Github

Cons:
Unless we fork and modify the plugin ourselves, we can't control which data is save to the database

Only report declared staged (Checkout + Post Actions aren't reported)
