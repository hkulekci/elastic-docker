FROM docker.elastic.co/elasticsearch/elasticsearch:6.0.0-rc1

RUN bin/elasticsearch-plugin install analysis-icu --batch
RUN bin/elasticsearch-plugin install ingest-attachment --batch
RUN bin/elasticsearch-plugin remove x-pack --purge

EXPOSE 9200:9200 9300:9300