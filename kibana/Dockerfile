FROM kibana:8.13.4

# RUN apt-get update && apt-get install -y netcat

COPY ./config/kibana.yml /opt/kibana/config/

COPY  entrypoint.sh /tmp/entrypoint.sh
USER root
RUN chmod +x /tmp/entrypoint.sh
USER kibana
ENTRYPOINT ["/bin/bash", "/tmp/entrypoint.sh"]
