ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
RUN logstash-plugin install logstash-integration-jdbc
ADD --chown=1000:0 https://jdbc.postgresql.org/download/postgresql-42.2.17.jar /usr/share/logstash/logstash-core/lib/jars/postgresql.jar
