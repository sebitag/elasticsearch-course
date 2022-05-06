# Section #1:
* Data is stored as Documents.
* A document's data is separated into Fields.
* Documents are JSON objects.
* How to query Elasticsearch? Vía a REST API.
* Written in JSON (Query DSL).
* Written by Java (based on Apache Lucene).
* Elastic Stack (former ELK stack).
* Elasticsearch [SEARCH,ANALYZE,STORE].
* Kibana (dashboard,web interface) [VISUALIZATION].
* Logstash (data processing pipeline) [DATA_INGESTION].
* X-Pack  (adds features to Kibana/Elasticsearch -security,monitoring,alerting,reporting,machine learning,graph relations,sql) [EXTRA_FEATURES].
* Beats (data collector) [DATA_INGESTION]
Common architecture:
* The application comunicates with Elasticsearch.
* Data will be stored both in the DB and Elasticsearch.
* You will need a script that imports data.

# Section #2:
* A Node is an instance of Elasticsearch that stores data.
* You can run any number of nodes on the same or different machines.
* Each node belongs to a Cluster (collection of nodes).
* Each unit of data that you store within your cluster is called a * Document.
* Documents are JSON objets + metadata (added by Elasticsearch).
* Every document within Elasticsearch is stored within an Index.
* An Index is a collection of logically related documents.
* Search queries are run against indices (noces.
* Each piece is reffered to as Shard.
* Sharding is done at the index level.
* A shard may be placed on any node.
* Format: HTTP_VERB /[API]/[COMMAND]
* For example: GET /_cluster/health
* Note: [API] Begins with an underscore by convention.
* There is a CAT API which outputs data into a human readable format.
## Sharding
* Sharding is a way to divide indices into smaller pieces.
* Each piece is reffered to as Shard.
* Sharding is done at the index level.
* A shard may be placed on any node.
* Why sharding?
  * Scale in data volume (able to store more documents).
  * Improve performance (parallelization of queries).