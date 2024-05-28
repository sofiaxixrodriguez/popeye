#FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder
#
#WORKDIR /app
#
#ADD . /app
#
#RUN mvn dependency:resolve
#RUN mvn package
#
#
#FROM eclipse-temurin:21-jre-alpine
#
#WORKDIR /app
#
#COPY --from=builder /app/target/worker-jar-with-dependencies.jar .
#
#CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
#
#FROM maven:3.5-jdk-8-alpine AS builder
#COPY . .
#RUN mvn dependency:resolve
#RUN mvn package
#
#FROM openjdk:8-jre-alpine
#WORKDIR /target
#COPY --from=builder /target .
#CMD java -jar worker-jar-with-dependencies.jar
#
FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder
COPY . .
RUN mvn dependency:resolve
RUN mvn package

FROM eclipse-temurin:21-jre-alpine
WORKDIR /target
COPY --from=builder /target .
CMD java -jar worker-jar-with-dependencies.jar
