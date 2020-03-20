FROM openjdk:8-jdk-alpine
VOLUME /tmp
ARG JAVA_OPTS
ENV JAVA_OPTS=$JAVA_OPTS
#RUN mvn clean install
ADD target/spring-cloud-consul-producer-0.0.1-SNAPSHOT.jar spring-cloud-consul-producer.jar
EXPOSE 8501
ENTRYPOINT exec java $JAVA_OPTS -jar spring-cloud-consul-producer.jar
# For Spring-Boot project, use the entrypoint below to reduce Tomcat startup time.
#ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar springbootstarter.jar
