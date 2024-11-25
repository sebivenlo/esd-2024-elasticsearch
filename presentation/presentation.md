---
marp: true
class: invert
---

<!-- paginate: true -->

![bg left height:6in](../imgs/this_repo.png)
https://github.com/sebivenlo/esd-2024-elasticsearch

---

![bg left height:6in](../imgs/elk_image.png)
https://github.com/deviantony/docker-elk

```
docker compose up setup
```
```
docker compose up
```
---

# <!--fit-->Elasticsearch + Kibana
Matej Kopecky, Leonie Böger
ESD Fall 2024

---

![bg left height:7in](../imgs/elastic_logo.jpg)
 - What is Elasticsearch + Elastic Stack
- Use Cases
- How does it work?
- Alternatives
- Clients
- Core concepts
- Searching
- Performance optimization

## TODO: LEONIE CONTENT
- Kibana



---

# What is it?

Elasticsearch is an open-source search and analytics engine that allows for:
- Quick, scalable and efficient searching
- Full-text searching
- Analyzing large amounts of data
- Storing large amounts of data

---

# What is it?

- Built on Apache Lucene (search engine library written in Java!)
- Distributed/multitenant-capable
- Communciation using REST endpoint interface
- NoSQL (schema-less JSON documents)
- 8th most popular DB-engine
- Most popular search engine

---

# History

- First released in 2010 as Elasticsearch
- Gained popularity due to search speed, full-text search capability, ability to handle large amounts of data (petabytes) and ability to horizontally scale well.
- Rebranded to Elastic Stack in 2015 with the addition of Kibana, Logstash and Beats.

---

![](../imgs/elk_stack.png)

---

# Use cases

Elasticsearch is used for a wide and growing range of use cases. Here are a few examples:
- Application search
- Web search
- Enterprise search
- Logging and log/data analytics
    - Infrastructure metrics
    - Container monitoring
    - Geospartial data analysis and visualization (ex. Flights from - to)


---

# Use Cases
- Volkswagen - uses Elasticsearch for log storage and Kibana for visualization.
- Airbus - Near Real-Time access to aircraft technical documents (2 billion blocks of technical documents, 3 000 queries per minute). Results under 2 seconds.
- Microsoft - Azure environment monitoring with Elasticsearch for longs and Kibana for visualizations.
- GitHub - search feature. 2 billion documents. Analytics to reveal rogue users and software bugs by indexing all alerts, events, logs and tracking rate of specific code exceptions.

---
## Alternatives
<style scoped>
table {
  font-size: 17px;
}
</style>

| Feature | Elasticsearch | Splunk |
|:---:|:---:|:---:|
| Scalability | High scalability with horizontal scaling across nodes | Scalable but may require more resources for larger datasets |  |  |
| Real-Time Capabilities | Near-instantaneous search and analytics | Real-time processing but can be resource-intensive |  |  |
| Data Ingestion | Supports various methods (APIs, Logstash, Beats) | Robust ingestion with Universal and Heavy Forwarders |  |  |
| Query Language | Powerful Query DSL for complex searches | SPL for creating queries and visualizations easily |  |  |
| Search Capabilities | Advanced full-text search with complex queries | Comprehensive search with AI-driven analytics |  |  |
| User Interface | CLI-based with some graphical tools | Highly intuitive and user-friendly |  |  |
| Cost | Open-source with optional paid features | Proprietary with licensing costs based on data volume |  |  |
| Integration | Extensive integrations with various data sources | Wide range of third-party integrations |  |  |
| Use Cases | Log and event data analysis, full-text search, analytics | searching, monitoring, and analyzing machine-generated big data |  |  |

---

# Licensing changes - OpenSearch?
![](../imgs/opensearch_logo.png)

---

# Licensing changes - OpenSearch?

- Amazon offered its own "AWS Elasticsearch" Software as a Service product. (Elasticsearch was offering SaaS product as well)
- Elastic AV argued Amazon is taking advantage of Elasticsearch and not contributing enough to the open-source project.
- In 2021 Elasticsearch introduced new licensing. It includes restrictions on the use of the software by cloud providers (mainly Amazon).
- Amazon and some developers argued the new license is no longer truly open-source and forked the last version using the old license under the name "OpenSearch".
- In September 2024, Elastic NV stated its goals have been met and added AGPLv3 open source license as one of the options.



---

## Core concepts
- documents
- what is an index (inverted index)

---

## Nodes and clusters
- nodes
- clusters

---

## Shards and Replicas
- shards
- replicas

---

## Setting up
- installation steps
- on premise vs cloud deployment
- basic config
- Elasticseach.yml file from github
https://github.com/elastic/elasticsearch/blob/main/distribution/src/config/elasticsearch.yml
- starting and stopping 

---

## Indexing data
- https://www.elastic.co/en/blog/found-elasticsearch-from-the-bottom-up#building-indexes
- adding a document to db
- inverted index
- dictionary and postings
- tokens

---

## Searching data
- search queries
- match, term and range queries
- advanced search
- filters
- keyword vs full-text search

---

## Kibana
- creating visualizations
- bar / pie charts, line graphs
- building dashboards

---

## performance optimization
- index strategies
- query optimizing
- hardware considerations (can leave that out)

## monitoring and maintenance
- monitoring tools
- Kibana
- APIs
- backup and restore
- scaling

## demo
- basic operations
- indexing a doc
- running query
- visualization with kabana

## assignment
- ??

