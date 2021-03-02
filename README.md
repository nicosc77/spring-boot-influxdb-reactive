# Reactive Spring Boot with InfluxDB 
Reactive API with InfluxDB 2 and Spring Webflux

## What is this?
The InfluxDB 2 reactive Java Client and Spring Webflux used in this Example enable reactive non-block streaming, reading and writing of metrics.
But influxdb-client-reactive as is doesn't allow infinite streaming with Spring webflux. This means unlike MongoDB with support for Tailable Cursors a stream will be closed if the InfluxDB query quits. An EventSource listener will start a new request after 3 seconds default idle. 
