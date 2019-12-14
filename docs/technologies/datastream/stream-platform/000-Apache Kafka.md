# Apache Kafka as Streaming Platform

## Status

Approved

## Context

A streaming platform has three key capabilities:

* Publish and subscribe to streams of records, similar to a message queue or enterprise messaging system.
* Store streams of records in a fault-tolerant durable way.
* Process streams of records as they occur (Kafka is not a stream processor)

As a Service solutions are not feasible due to costs.

## Decision

Use [Apache Kafka](https://kafka.apache.org/) to stream data from and to different sources using both:
* queue approach
* publish/subscriber approach

Apache Kafka also adds a persistence layer 

## Consequences

Kafka is generally used for two broad classes of applications:

* Building real-time streaming data pipelines that reliably get data between systems or applications
* Building real-time streaming applications that transform or react to the streams of data
* To understand how Kafka does these things, let's dive in and explore Kafka's capabilities from the bottom up.

First a few concepts:

* Kafka is run as a cluster on one or more servers that can span multiple datacenters.
* The Kafka cluster stores streams of records in categories called topics.
* Each record consists of a key, a value, and a timestamp.


Pros:
* Battle proof
* Highly scalable
* Used under the hood by cloud/as a service solutions
* Built in persistence of events (events log)
* Supports queue and publish/subscribe combined together
* Can be deployed in several ways:
  * Hadoop cluster
  * AWS
  * Kubernetes ?

Cons:
* Requires dev-ops and maintainance 
* Requires dev-ops and maintainance for the persistence layer