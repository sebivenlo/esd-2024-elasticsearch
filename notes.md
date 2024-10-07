# Introduction

## What is it + Elastic Stack
Elasticsearch is an open-source search and analytics engine that allows for quick,
scalable, and efficient searching, analyzing, and storing of large volumes of data. It's built
on Apache Lucene and provides a distributed, multitenant-capable full-text search
engine with an HTTP RESTful interface and schema-free JSON documents. Elasticsearch
is widely used for log and event data analysis, real-time application monitoring, and
search functionalities across various types of documents.
https://www.elastic.co/guide/en/elasticsearch/reference/current/elasticsearch-intro-what-is-es.html

Based on Apache Lucene (Java!).


## History
## Use cases + companies
Elasticsearch is used for a wide and growing range of use cases. Here are a few examples:

Observability

Logs, metrics, and traces: Collect, store, and analyze logs, metrics, and traces from applications, systems, and services.
Application performance monitoring (APM): Monitor and analyze the performance of business-critical software applications.
Real user monitoring (RUM): Monitor, quantify, and analyze user interactions with web applications.
OpenTelemetry: Reuse your existing instrumentation to send telemetry data to the Elastic Stack using the OpenTelemetry standard.
Search

Full-text search: Build a fast, relevant full-text search solution using inverted indexes, tokenization, and text analysis.
Vector database: Store and search vectorized data, and create vector embeddings with built-in and third-party natural language processing (NLP) models.
Semantic search: Understand the intent and contextual meaning behind search queries using tools like synonyms, dense vector embeddings, and learned sparse query-document expansion.
Hybrid search: Combine full-text search with vector search using state-of-the-art ranking algorithms.
Build search experiences: Add hybrid search capabilities to apps or websites, or build enterprise search engines over your organization’s internal data sources.
Retrieval augmented generation (RAG): Use Elasticsearch as a retrieval engine to supplement generative AI models with more relevant, up-to-date, or proprietary data for a range of use cases.
Geospatial search: Search for locations and calculate spatial relationships using geospatial queries.
Security

Security information and event management (SIEM): Collect, store, and analyze security data from applications, systems, and services.
Endpoint security: Monitor and analyze endpoint security data.
Threat hunting: Search and analyze data to detect and respond to security threats.



---

# Alternatives
## Comparisons

---

# Core concepts
## Documents
## What is an index (inverted index)

---

# Nodes and clusters
## Nodes
## Clusters

---

# Shards and Replicas
## Shards
## Eeplicas

---

# Setting up
## Installation steps
## On premise vs cloud deployment
## Basic config
## Elasticseach.yml file from github
https://github.com/elastic/elasticsearch/blob/main/distribution/src/config/elasticsearch.yml
## Starting and stopping 

---

# Indexing data
 https://www.elastic.co/en/blog/found-elasticsearch-from-the-bottom-up#building-indexes
## Adding a document to db
## Inverted index
## Dictionary and postings
## Tokens

---

# Searching data
## Search queries
## Match, term and range queries
## Ddvanced search
## Filters
## Keyword vs full-text search

---

# Kibana
## Creating visualizations
## Bar / pie charts, line graphs
## Building dashboards

---

# Performance optimization
## Index strategies
## Query optimizing
## Hardware considerations (can leave that out)

# Monitoring and maintenance
## Monitoring tools
## Kibana
## APIs
## Backup and restore
## Scaling

# Demo
## Basic operations
## Indexing a doc
## Running query
## Visualization with kabana

# Assignment
- ??

