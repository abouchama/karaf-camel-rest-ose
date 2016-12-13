FROM jboss-fuse-6/fis-karaf-openshift:1.0
MAINTAINER docker-maven-plugin@jolokia.org
ENV HTTP_PORT=9191
EXPOSE 9191
COPY maven /deployments/
USER root
RUN ["chown", "-R", "jboss:jboss","/deployments/"]

USER jboss
CMD /deployments/deploy-and-run.sh
