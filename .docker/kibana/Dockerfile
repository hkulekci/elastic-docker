FROM openjdk:8-jre

ENV KB_PKG_NAME kibana-4.1.11

RUN wget https://download.elastic.co/kibana/kibana/$KB_PKG_NAME-linux-x64.tar.gz
RUN \
  cd / && \
  wget https://download.elastic.co/kibana/kibana/$KB_PKG_NAME-linux-x64.tar.gz && \
  tar xvzf $KB_PKG_NAME-linux-x64.tar.gz && \
  rm -f $KB_PKG_NAME-linux-x64.tar.gz && \
  mv /$KB_PKG_NAME-linux-x64 /kibana

CMD ["/kibana/bin/kibana"]

ENV ELASTICSEARCH_URL "http://elasticsearch:9200"
EXPOSE 5601:5601