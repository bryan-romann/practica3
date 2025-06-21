FROM maven:3.8.5-openjdk-17 as build
COPY . .
RUN mvn clean package -DskipTests

FROM openjdk:17.0.1-jdk-slim
COPY --from=build /target/practica3.jar practica3.jar
EXPOSE 91
ENTRYPOINT ["java", "jar", "practica3.jar"]