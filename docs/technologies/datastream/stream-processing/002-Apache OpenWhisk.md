# Apache OpenWhisk as Serverless Platform

## Status

Proposed

## Context

Any kind of data is produced as a stream of events. Credit card transactions, sensor measurements, machine logs, or user interactions on a website or mobile application, all of these data are generated as a stream.

Data can be processed as unbounded or bounded streams.

1. Unbounded streams have a start but no defined end. They do not terminate and provide data as it is generated. Unbounded streams must be continuously processed, i.e., events must be promptly handled after they have been ingested. It is not possible to wait for all input data to arrive because the input is unbounded and will not be complete at any point in time. Processing unbounded data often requires that events are ingested in a specific order, such as the order in which events occurred, to be able to reason about result completeness.

2. Bounded streams have a defined start and end. Bounded streams can be processed by ingesting all data before performing any computations. Ordered ingestion is not required to process bounded streams because a bounded data set can always be sorted. Processing of bounded streams is also known as batch processing.

As a Service solutions are not feasible due to costs.

Use cases are simple.

## Decision

Consider [Apache OpenWhisk](https://openwhisk.apache.org/) as serverless platform

## Consequences

Apache OpenWhisk is an open source, distributed Serverless platform that executes functions (fx) in response to events at any scale. OpenWhisk manages the infrastructure, servers and scaling using Docker containers so you can focus on building amazing and efficient applications.

The OpenWhisk platform supports a programming model in which developers write functional logic (called Actions), in any supported programming language, that can be dynamically scheduled and run in response to associated events (via Triggers) from external sources (Feeds) or from HTTP requests. The project includes a REST API-based Command Line Interface (CLI) along with other tooling to support packaging, catalog services and many popular container deployment options.


Pros:
* Serverless architecture allows everyone to write actions following events
* Highly scalable
* Integrated with several other tools
  * Slack
  * Github
  * JIRA
  * Push notifications for mobile apps
  * [Kafka](https://developer.ibm.com/patterns/serverless-event-stream-processing/) 
* Supports almost any language
  * Javascript (NodeJS)
  * GO
  * Ruby
  * Python
  * Java
* Can be deployed in several ways:
  * Docker compose
  * Mesos
  * Kubernetes

Cons:
* Is a serverless platform which might be used for stream processing, is not design only for that scope
* Requires dev-ops and maintainance