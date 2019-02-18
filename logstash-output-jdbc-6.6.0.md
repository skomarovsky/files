# HOW-TO

**To create Offline Plugin Pack using docker:**

*docker run --rm -it --name logstash --mount type=bind,source=/opt/data/logstash,destination=/opt/data/logstash logstash:6.6.0 /bin/bash*
*cd /usr/share/logstash*
*bin/logstash-plugin install logstash-output-jdbc*
*bin/logstash-plugin prepare-offline-pack --output logstash-output-jdbc-6.6.0.zip logstash-output-jdbc*
*cp logstash-output-jdbc-6.6.0.zip /opt/data/logstash*
