## Fluentd Config Examples

Repository for storing example Fluentd configurations, so that I don't forget how to re-create them.

#### Fluentd docker Image

`src` contains a Dockerfile for a alpine based image, derived from instructions found here: https://hub.docker.com/r/fluent/fluentd/

#### Multiple Destinations with Regex Filter

`mutliple-destinations-filter` contains an example of sending logs to two different destinations, one for error logs, the other for success logs. Fluentd config files represent a 'pipe' that log events pass through- the `@type copy` forks the pipe and sends all logs to each `<label>` element.

#### Multiple Destinations with Regex Filter

`mutliple-destinations-sample` also sends to two destinations, but solves a different use case. Here, a sample of 1/100 of the logs are sent to one destination for analysis, while all logs are sent to the other for long term storage. 
