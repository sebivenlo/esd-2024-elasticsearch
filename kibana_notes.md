# Kibana Notes

## [Observe](https://www.elastic.co/kibana#observability)
- Kibana Lens for data and search analytics
- Discover for unstructured data
- Time series analysis
- AI Ops

## Search Analysis
- analysing search queries from users, optimizing search based on analytics
### [App Search Analytics](https://www.elastic.co/blog/what-your-elastic-app-search-analytics-are-telling-you)
most used app search analytics:
#### query analytics
- most frequent ones & ones with no result
-> identify and close gaps in data, improve customer satisfaction (they search for sth but are not finding it)
- select date range 
    - top queries are displayed showing search terms 
    - number of queries produced by that term 
    - how many clicks occured on that term
    - <mark>TODO add screenshot from our example or link
    - add synonyms for search terms
#### click analytics

#### recent queries

## Comparison to [Grafana](https://logz.io/blog/grafana-vs-kibana/)

|Comparison point|Kibana|Grafana|
|-|-|-|
|Purpose|Monitoring resources (CPU, disk, memory, network usage)|Monitoring logs, full-text querying
|Data Sources|Elasticsearch only|optimal for time-series data (e.g. InfluxDB), PostgreSQL, Elasticsearch and more using plugins|
|License|Closed-source beyond version 7.9|Free and open-source (FOSS/OSS)|
|Access Control|Access control is behind paywall|Has built-in user control|
|Querying|- Kibana Query Language (KQL) only filters <br> - Lucene is more powerful but is more complex to learn|Query Editor's syntax varies depending on the data source|
|Functionality|Many visualization options|More customization options, editing is easier (e.g. collapsible rows)|
|Alerting|Possible|Possible|
|Community|[Active open-source community](https://github.com/elastic/kibana/graphs/commit-activity)|[Active open-source community](https://github.com/grafana/grafana/graphs/commit-activity) as well|