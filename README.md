## ci-tools Logstash

Implement logstash logging directly inside ci-tools.

**Pros:**  
1. We have complete control of what we log and the format
2. We are independant of any build system we use (jenkins, github actions, gitlab)

**Cons:**  
1. 100% our responsability to implement and maintain (time consuming)
2. Being independant from the build system means we don't have any information about it
   1. ci-tools doesn't know about Jenkins stages
   2. it doesn't know anything before or after it's own execution (i.e. check out time, build monitoring vs build *machine* monitoring)

## [Jenkins Logstash plugin](https://plugins.jenkins.io/logstash/)

**Pros:**  
1. Allows us to easily control the information sent to the stash using the `logstash` step
2. Can output the complete build output using `logstashSend` step as a post action

**Cons:**  
1. The plugins sends each output line as an individual log (a single command with a multi-line output will generate multiple log entry)
2. We don't control the fields sent unless we modify the plugin (open source, so we could fork it)
  1. The build time is cummulative for all log entry, so if we want the build time of a single stage, we need to work around that limitation (might require complex Kibana query)
  2. The more we go outside what it offers, the more work we need to do
3. Jenkins specific

[Basic Kibana example](ELK_build_time.png)

## [Jenkins Job and Stage Monitoring plugin + Graphana](https://plugins.jenkins.io/github-autostatus/)

**Pros:**  
1. Very simple to setup visualization (the plugin output to an InfluxDB and Graphana queries from it)
2. Supports Global build time, stages build time and test reporting (coverage/Test Cases/etc...) out of the box (the latter one has not been tested)
3. Could allow us to see the stages in Github

**Cons:**  
1. Unless we fork and modify the plugin ourselves, we can't control which data is save to the database
2. Only report declared staged (Checkout + Post Actions aren't reported)
3. Jenkins specific

[Basic Graphana example](Graphana_build_time.png)