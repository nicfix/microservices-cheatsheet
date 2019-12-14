# Use Faust for stream processing

## Status

Proposed

## Context

Any kind of data is produced as a stream of events. Credit card transactions, sensor measurements, machine logs, or user interactions on a website or mobile application, all of these data are generated as a stream.

Data can be processed as unbounded or bounded streams.

1. Unbounded streams have a start but no defined end. They do not terminate and provide data as it is generated. Unbounded streams must be continuously processed, i.e., events must be promptly handled after they have been ingested. It is not possible to wait for all input data to arrive because the input is unbounded and will not be complete at any point in time. Processing unbounded data often requires that events are ingested in a specific order, such as the order in which events occurred, to be able to reason about result completeness.

2. Bounded streams have a defined start and end. Bounded streams can be processed by ingesting all data before performing any computations. Ordered ingestion is not required to process bounded streams because a bounded data set can always be sorted. Processing of bounded streams is also known as batch processing.

As a Service solutions are not feasible due to costs.

The use cases are simple.


## Decision

Consider using [Faust](https://faust.readthedocs.io/en/latest/index.html) to process data streams in simple Use Cases.

## Consequences

Faust is a stream processing library, porting the ideas from Kafka Streams to Python.

It is used at Robinhood to build high performance distributed systems and real-time data pipelines that process billions of events every day.

Faust provides both stream processing and event processing, sharing similarity with tools such as Kafka Streams, Apache Spark/Storm/Samza/Flink,

It does not use a DSL, it’s just Python! This means you can use all your favorite Python libraries when stream processing: NumPy, PyTorch, Pandas, NLTK, Django, Flask, SQLAlchemy, ++


Pros:
* Simple
* Idiomatic Python interface
* Integrable in any python application using it as a pip package
* Can use kafka or amqp

Cons:
* Library, not framework
  * No loggin facility out of the box
  * No monitoring tools out of the box
  * No metrics out of the box
* Requires some deployed app to integrate it
* Not the same level of sofistication of solutions such as Apache Flink