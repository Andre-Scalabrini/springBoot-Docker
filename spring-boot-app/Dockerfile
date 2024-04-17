FROM ubuntu:latest

RUN apt-get update && apt-get clean

RUN apt-get install -y openjdk-11-jdk

VOLUME /tmp

EXPOSE 8080

ARG JAR_FILE=target/spring-boot-docker.jar

ADD ${JAR_FILE} app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
