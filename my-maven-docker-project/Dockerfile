FROM openjdk:8
ADD target/my-maven-docker-project.jar my-maven-docker-project.jar
RUN echo "This is a Docker Build Jenkins Step" > out.txt
ENTRYPOINT ["java", "-jar","my-maven-docker-project.jar"]
EXPOSE 8080