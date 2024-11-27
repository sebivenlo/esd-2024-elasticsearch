
# Setup and check

### 1. Set up Elasticsearch container

Clone [this](https://github.com/deviantony/docker-elk) repo and open terminal in the directory.
Run these commands:
```bash
docker compose up setup
```
```bash
docker compose up
```
give it a few minutes to load...

### 2. Check if Elasticsearch and Kibana are running
Open [http://localhost:9200](http://localhost:9200) in your browser, use username ```elastic``` and password ```changeme```

the JSON body response should look similar to this:

```json
{
    "name": "elasticsearch",
    "cluster_name": "docker-cluster",
    "cluster_uuid": "TY2HrE-8QH6MLRfMdqdDMQ",
    "version": {
        "number": "8.16.0",
        "build_flavor": "default",
        "build_type": "docker",
        "build_hash": "12ff76a92922609df4aba61a368e7adf65589749",
        "build_date": "2024-11-08T10:05:56.292914697Z",
        "build_snapshot": false,
        "lucene_version": "9.12.0",
        "minimum_wire_compatibility_version": "7.17.0",
        "minimum_index_compatibility_version": "7.0.0"
    },
    "tagline": "You Know, for Search"
}
```

Open [http://localhost:5601](http://localhost:5601) in your browser, use username ```elastic``` and password ```changeme```.
Kibana home screen should open.

### 3. Open Elastic Dev Tools Console

On bottom left click on "Dev Tools". You should be on this screen:

![](../imgs/kibana_console.png)




---

# Play around assignment

## 1. Create Movies index
Create an index called "movies" in Dev console, with following fields:

- title
- director
- year
- genre
- rating

Figure out the mapping types.

**Help**:<br>
https://www.elastic.co/guide/en/elasticsearch/reference/current/indices-create-index.html#mappings

https://opster.com/guides/elasticsearch/glossary/elasticsearch-data-types/


### Solution:
```
PUT /movies
{
  "mappings": {
    "properties": {
      "title": { "type": "text" },
      "director": { "type": "text" },
      "year": { "type": "integer" },
      "genre": { "type": "keyword" },
      "rating": { "type": "float" }
    }
  }
}
```


## 2. Add a document to the movies index
Add the following movie to the index:

Title: "The Shawshank Redemption", Director: "Frank Darabont", Year: 1994, Genre: "Drama", Rating: 9.3

**Help**:<br>
https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-index_.html#docs-index-api-example

https://opster.com/guides/elasticsearch/glossary/elasticsearch-document/

### Solution:
```
POST /movies/_doc/1
{
  "title": "The Shawshank Redemption",
  "director": "Frank Darabont",
  "year": 1994,
  "genre": "Drama",
  "rating": 9.3
}
```


### 2.1. Add following movies to the movies index:
```
POST /_bulk
{ "index": { "_index": "movies", "_id": "2" } }
{ "title": "The Godfather", "director": "Francis Ford Coppola", "year": 1972, "genre": "Crime", "rating": 9.2 }
{ "index": { "_index": "movies", "_id": "3" } }
{ "title": "The Dark Knight", "director": "Christopher Nolan", "year": 2008, "genre": "Action", "rating": 9.0 }
{ "index": { "_index": "movies", "_id": "4" } }
{ "title": "Pulp Fiction", "director": "Quentin Tarantino", "year": 1994, "genre": "Crime", "rating": 8.9 }
{ "index": { "_index": "movies", "_id": "5" } }
{ "title": "Fight Club", "director": "David Fincher", "year": 1999, "genre": "Drama", "rating": 8.8 }
{ "index": { "_index": "movies", "_id": "6" } }
{ "title": "Inception", "director": "Christopher Nolan", "year": 2010, "genre": "Sci-Fi", "rating": 8.8 }
{ "index": { "_index": "movies", "_id": "7" } }
{ "title": "Forrest Gump", "director": "Robert Zemeckis", "year": 1994, "genre": "Drama", "rating": 8.8 }
{ "index": { "_index": "movies", "_id": "8" } }
{ "title": "The Lord of the Rings: The Return of the King", "director": "Peter Jackson", "year": 2003, "genre": "Fantasy", "rating": 8.9 }
{ "index": { "_index": "movies", "_id": "9" } }
{ "title": "The Good, the Bad and the Ugly", "director": "Sergio Leone", "year": 1966, "genre": "Western", "rating": 8.8 }
{ "index": { "_index": "movies", "_id": "10" } }
{ "title": "The Godfather: Part II", "director": "Francis Ford Coppola", "year": 1974, "genre": "Crime", "rating": 9.0 }
{ "index": { "_index": "movies", "_id": "11" } }
{ "title": "The Lord of the Rings: The Fellowship of the Ring", "director": "Peter Jackson", "year": 2001, "genre": "Fantasy", "rating": 8.8 }
{ "index": { "_index": "movies", "_id": "12" } }
{ "title": "Star Wars: Episode V - The Empire Strikes Back", "director": "Irvin Kershner", "year": 1980, "genre": "Sci-Fi", "rating": 8.7 }
{ "index": { "_index": "movies", "_id": "13" } }
{ "title": "The Lord of the Rings: The Two Towers", "director": "Peter Jackson", "year": 2002, "genre": "Fantasy", "rating": 8.7 }
{ "index": { "_index": "movies", "_id": "14" } }
{ "title": "The Matrix", "director": "Lana Wachowski, Lilly Wachowski", "year": 1999, "genre": "Sci-Fi", "rating": 8.7 }
{ "index": { "_index": "movies", "_id": "15" } }
{ "title": "Goodfellas", "director": "Martin Scorsese", "year": 1990, "genre": "Crime", "rating": 8.7 }
```

## 3. Search queries

### 3.1. Write a query to find all movies directed by "Christopher Nolan".
Solution:
```
GET /movies/_search
{
  "query": {
    "match": {
      "director": "Christopher Nolan"
    }
  }
}
```
### 3.2. Write a query to find all movies with rating greather than 8.7 .
Solution:
```
GET /movies/_search
{
  "query": {
    "range": {
      "rating": {
        "gt": 8.7
      }
    }
  }
}
```
### 3.3. Write a query to find all movies with "Fantasy" genre.
Solution:
```
GET /movies/_search
{
  "query": {
    "match": {
      "genre": "Fantasy"
    }
  }
}
```
### 3.4. Write a query to find all "Crime" genre movies released before the year 2000.
Solution:
```
GET /movies/_search
{
  "query": {
    "bool": {
      "must": [
        { "match": { "genre": "Crime" } },
        { "range": { "year": { "lt": 2000 } } }
      ]
    }
  }
}
```
### 3.5. BONUS: Write a query to find all movies released between the years 1990 and 2000 with a rating between 8.5 and 9.0.
Solution:
```
GET /movies/_search
{
  "query": {
    "bool": {
      "must": [
        {
          "range": {
            "year": {
              "gte": 1990,
              "lte": 2000
            }
          }
        },
        {
          "range": {
            "rating": {
              "gte": 8.5,
              "lte": 9.0
            }
          }
        }
      ]
    }
  }
}
```

**Help**:<br>
https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-match-query.html
https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-bool-query.html
https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-range-query.html









