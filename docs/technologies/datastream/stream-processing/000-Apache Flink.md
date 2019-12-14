# Apache Flink as Streaming Processor

## Status

Proposed

## Context

Any kind of data is produced as a stream of events. Credit card transactions, sensor measurements, machine logs, or user interactions on a website or mobile application, all of these data are generated as a stream.

Data can be processed as unbounded or bounded streams.

1. Unbounded streams have a start but no defined end. They do not terminate and provide data as it is generated. Unbounded streams must be continuously processed, i.e., events must be promptly handled after they have been ingested. It is not possible to wait for all input data to arrive because the input is unbounded and will not be complete at any point in time. Processing unbounded data often requires that events are ingested in a specific order, such as the order in which events occurred, to be able to reason about result completeness.

2. Bounded streams have a defined start and end. Bounded streams can be processed by ingesting all data before performing any computations. Ordered ingestion is not required to process bounded streams because a bounded data set can always be sorted. Processing of bounded streams is also known as batch processing.

As a Service solutions are not feasible due to costs.


## Decision

Consider [Apache Flink](https://flink.apache.org/) to process data streams.

## Consequences

Apache Flink is a framework and distributed processing engine for stateful computations over unbounded and bounded data streams. Flink has been designed to run in all common cluster environments, perform computations at in-memory speed and at any scale.

Apache Flink excels at processing unbounded and bounded data sets. Precise control of time and state enable Flink’s runtime to run any kind of application on unbounded streams. Bounded streams are internally processed by algorithms and data structures that are specifically designed for fixed sized data sets, yielding excellent performance.


Pros:
* Battle proof
* Highly scalable
* Monitoring, metrics and logging out of the box
* Can be deployed in several ways:
  * Hadoop cluster
  * Mesos
  * Kubernetes

Cons:
* Application programming interface limited:
  * Java (full capabilities)
  * Python (Table API, only the highest level, lowest expressiveness)
* Requires dev-ops and maintainance 