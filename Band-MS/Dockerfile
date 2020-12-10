FROM openjdk:8-jdk-alpine
VOLUME /tmp
ARG JAVA_OPTS
ENV JAVA_OPTS=$JAVA_OPTS
ADD ondo-band-microservice.jar ondo-band-microservice.jar
ADD application.yml application.yml
#EXPOSE 3333
#ENTRYPOINT exec java $JAVA_OPTS -jar ondomsjars.jar
# For Spring-Boot project, use the entrypoint below to reduce Tomcat startup time.
#ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar ondomsjars.jar
#ENTRYPOINT exec java $JAVA_OPTS -Dspring.config.name=application.yml -Djava.security.egd=file:/dev/./urandom -jar ondo-band-microservice.jar

ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar ondo-band-microservice.jar