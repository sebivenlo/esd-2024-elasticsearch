# Kibana Assignment

### Adding data source

Data source:
- IMDB top movies

## 1. Discover data

In the Discover tab, choose the IMDB data view as data source.

### 1.1 Filtering IMDB Ratings
Filter the data so that only movies with an IMDB rating of 8 or over are shown.
The filtering is done using [Kibana Query Language or Kuery](https://www.elastic.co/guide/en/kibana/8.16/kuery-query.html) by default. 

### 1.2 Filtering Genres
Additionally to the previous filter, show only movies which include the 'Drama' genre (among other genres).

### 1.3 Bonus Question
Why is the correct answer not a recommended search practice in most cases? <br>
Hint: Have a look at the extensive [documentation](https://www.elastic.co/guide/en/elasticsearch/reference/8.16/query-dsl-query-string-query.html#query-string-wildcard).


## 2. Create a dashboard
### 2.1 Visualize Top Directors
Create a visualization that shows only the top 5 directors and how many movies they directed that are part of the list.
### 2.2 Visualize IMDB Ratings
Create a visualization that shows how often an IMDB rating was given in a range of ca. 0.2 steps.
### Filtering data in Dashboard
Filter the visualizations to only consider movies with an IMBD rating of over 8.5.