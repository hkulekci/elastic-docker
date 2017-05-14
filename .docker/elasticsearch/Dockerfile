FROM elasticsearch:5.4.0

RUN bin/elasticsearch-plugin install x-pack
RUN bin/elasticsearch-plugin install analysis-icu

EXPOSE 9200:9200 9300:9300