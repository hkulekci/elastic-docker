FROM elasticsearch:latest

RUN bin/elasticsearch-plugin install x-pack
RUN bin/elasticsearch-plugin install analysis-icu

EXPOSE 9200:9200 9300:9300