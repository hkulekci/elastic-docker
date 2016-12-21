FROM kibana:latest

RUN kibana-plugin install x-pack

ENV ELASTICSEARCH_URL "http://elasticsearch:9200"

EXPOSE 5601:5601