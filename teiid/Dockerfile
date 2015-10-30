# Use latest jboss/base-jdk:7 image as the base
FROM jboss/base-jdk:8
MAINTAINER Luca Gioppo <gioppoluca@libero.it>
ENV JBOSS_HOME /opt/jboss/jbossas

RUN cd $HOME \
  && curl -O https://repository.jboss.org/nexus/service/local/repositories/relea
ses/content/org/jboss/teiid/teiid/8.12.0.Final/teiid-8.12.0.Final-server.zip \
  && unzip teiid-8.12.0.Final-server.zip \
  && mv $HOME/teiid-8.12.0.Final $JBOSS_HOME \
  && rm teiid-8.12.0.Final-server.zip

EXPOSE 8080 9999 9990 4447

CMD ["/opt/jboss/jbossas/bin/standalone.sh", "-b", "0.0.0.0"]