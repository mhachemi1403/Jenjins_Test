FROM openjdk:8-jdk-alpine
ADD target/application.jar /application.jar
RUN sh -c "touch /application.jar"
ENTRYPOINT [ "sh", "-c", "java -jar /application.jar"]