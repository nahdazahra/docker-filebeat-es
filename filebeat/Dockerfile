FROM docker.elastic.co/beats/filebeat:6.4.3

# Copy our custom configuration file
COPY --chown=root:root filebeat.yml /usr/share/filebeat/filebeat.yml

USER root
# Change owner to access docker log files in logs in filebeat/logs
RUN chown -R root /usr/share/filebeat/
RUN chmod -R go-w /usr/share/filebeat/
