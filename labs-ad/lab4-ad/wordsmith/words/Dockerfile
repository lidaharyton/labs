FROM maven:3.8.6-openjdk-11 AS build
WORKDIR /usr/src/app
COPY pom.xml.
COPY src ./src
RUN mvn package -DskipTests

FROM openjdk:11-jre-slim
WORKDIR /usr/src/app
COPY --from=build /usr/src/app/target/words.jar ./words.jar
CMD ["java", "-jar", "words.jar"]
