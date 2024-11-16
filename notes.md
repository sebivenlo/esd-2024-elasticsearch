# Introduction

## What is it + Elastic Stack
Elasticsearch is an open-source search and analytics engine that allows for quick, scalable, and efficient searching, analyzing, and storing of large volumes of data.
It's built on Apache Lucene (search engine library written in Java!) and provides a distributed, multitenant-capable (mode of operation of software where multiple independent instances of one or multiple applications operate in a shared environment) full-text search engine with an HTTP RESTful interface and schema-free JSON documents.
Elasticsearch is widely used for log and event data analysis, real-time application monitoring, and search functionalities across various types of documents.
https://www.elastic.co/guide/en/elasticsearch/reference/current/elasticsearch-intro-what-is-es.html
https://sue.nl/wp-content/uploads/sites/8/2022/07/elastic-logo-920x920-sue-v02.png


## History
First released in 2010. Gained popularity due to ability to scale (horizontal scaling via adding nodes to cluster) and handle large amounts of data.

Rebranded to Elastic Stack in 2015, with additional tools - Kibana, Logstash and Beats.
https://www.michael-wutzke.com/wp-content/uploads/2019/02/how-it-works-elastic-stack-beats-logstash-elasticsearch-kibana.png

## Use cases
Elasticsearch is used for a wide and growing range of use cases. Here are a few examples:

## Content Search Engine
Elasticsearch doesn't use concepts as primary keys or relations, since it is a schema-free/less JSON data storage. You might have noticed, I haven't used word database anywhere. It also isn't ACID complaint.

Full-text search: Build a fast, relevant full-text search solution using inverted indexes, tokenization, and text analysis. (We're gonna explain those, don't worry!)
Vector storage: Store and search vectorized data, and create vector embeddings with built-in and third-party natural language processing (NLP) models.
Semantic search: Understand the intent and contextual meaning behind search queries using tools like synonyms, dense vector embeddings, and learned sparse query-document expansion.
Hybrid search: Combine full-text search with vector search using modern ranking algorithms.
Build search experiences: Add hybrid search capabilities to apps or websites, or build enterprise search engines over your organization’s internal data sources.


## Use examples
Volkswagen - uses Elasticsearch for long storage and Kibana for visualization.
https://www.elastic.co/elasticon/tour/2017/munich/distributed-logging-and-monitoring-at-volkswagen-using-the-elastic-stack

Airbus - Near Real-Time access to aircraft technical documents (2 billion blocks of technical documents, 3 000 queries per minute). Results under 2 seconds.
https://www.elastic.co/customers/airbus

Microsoft - Azure environment monitoring with Elasticsearch for longs and Kibana for visualizations.
https://www.elastic.co/elasticon/conf/2018/sf/monitor-your-cloud-environment-with-the-logstash-azure-monitoring-module

GitHub - search feature. 2 billion documents. Analytics to reveal rogue users and software bugs by indexing all alerts, events, logs and tracking rate of specific code exceptions.
https://www.elastic.co/customers/github




---

# Alternatives
https://coralogix.com/guides/elasticsearch/elasticsearch-vs-opensearch-key-differences/
https://bigdataboutique.com/blog/opensearch-vs-elasticsearch-an-up-to-date-comparison-5c1c71
https://typesense.org/
https://www.meilisearch.com/
https://manticoresearch.com/

## Comparisons (to SQL as well?)

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

# Indexing data (CRUD examples)
 https://www.elastic.co/en/blog/found-elasticsearch-from-the-bottom-up#building-indexes
## Adding a document to db
## Inverted index
## Dictionary and postings
## Tokens

---

# Searching data
## Search queries
## Match, term and range queries
## Advanced search
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



# Sources

https://medium.com/tech-explained/elasticsearch-explained-411e300413c7
https://medium.com/tech-explained/4-steps-to-setting-up-the-perfect-elasticsearch-test-environment-7d7ccf4bdeb9
https://medium.com/tech-explained/getting-hands-on-with-elasticsearch-9969a2894f8a

(freedium.cfd *cough cough*)

https://www.elastic.co/guide/en/elasticsearch/reference/current/elasticsearch-intro-what-is-es.html
https://www.elastic.co/customers/success-stories
https://www.youtube.com/playlist?list=PL_mJOmq4zsHbcdoeAwNWuhEWwDARMMBta
