FROM adoptopenjdk/openjdk11:jre-11.0.8_10-alpine
RUN mkdir /opt/app
COPY blog-0.0.1-SNAPSHOT.jar /opt/app
COPY xray-daemon/xray /usr/bin/xray-daemon
EXPOSE 80
CMD ["sh", "-c", "xray-daemon -f /var/log/xray-daemon.log &; java -jar /opt/app/blog-0.0.1-SNAPSHOT.jar"]
