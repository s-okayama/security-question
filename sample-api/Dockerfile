FROM maven:3.9.6-eclipse-temurin-21-alpine
WORKDIR /sample-api
COPY . /sample-api
RUN mvn package

CMD ["java", "-jar", "sample-api.jar"]