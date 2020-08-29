FROM adoptopenjdk/openjdk11:jre-11.0.8_10-alpine
RUN mkdir /opt/app
COPY blog-0.0.1-SNAPSHOT.jar /opt/app
EXPOSE 80
CMD ["sh", "-c", "java -jar /opt/app/blog-0.0.1-SNAPSHOT.jar"]
