# Pull base image.
FROM openjdk:8-jre

ENV ES_PKG_NAME elasticsearch-1.7.4

# Install Elasticsearch.
RUN \
  cd / && \
  wget https://download.elasticsearch.org/elasticsearch/elasticsearch/$ES_PKG_NAME.tar.gz && \
  tar xvzf $ES_PKG_NAME.tar.gz && \
  rm -f $ES_PKG_NAME.tar.gz && \
  mv /$ES_PKG_NAME /elasticsearch

# Define mountable directories.
VOLUME ["/data"]

# Mount elasticsearch.yml config
ADD config/elasticsearch.yml /elasticsearch/config/elasticsearch.yml

# Define working directory.
WORKDIR /data

RUN /elasticsearch/bin/plugin install elasticsearch/elasticsearch-analysis-icu/2.7.0
RUN /elasticsearch/bin/plugin install com.yakaz.elasticsearch.plugins/elasticsearch-action-updatebyquery/2.6.0
RUN /elasticsearch/bin/plugin install gr.skroutz/elasticsearch-analysis-turkishstemmer/0.1.9

# Define default command.
CMD ["/elasticsearch/bin/elasticsearch"]

# Expose ports.
#   - 9200: HTTP
#   - 9300: transport
EXPOSE 9200
EXPOSE 9300