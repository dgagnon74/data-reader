# Start with a base image containing Java runtime (mine java 8)
FROM openjdk:8u212-jdk-slim
# Add Maintainer Info
LABEL maintainer="david.gagnon@gmail.com"
# Add a volume pointing to /tmp
VOLUME /tmp
# Make port 8080 available to the world outside this container
EXPOSE 9091
# The application's jar file (when packaged)
ARG JAR_FILE=target/data-reader-0.0.1-SNAPSHOT.jar
# Add the application's jar to the container
ADD ${JAR_FILE} codestatebkend.jar
# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/codestatebkend.jar"]