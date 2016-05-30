FROM gcr.io/google_appengine/openjdk8
VOLUME /tmp
ADD helloworld-springboot-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT [ "java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
