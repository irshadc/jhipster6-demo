FROM adoptopenjdk/openjdk11:jre-11.0.8_10-alpine
RUN mkdir /opt/app
COPY blog-0.0.1-SNAPSHOT.jar /opt/app
COPY xray-daemon/xray /usr/bin/xray-daemon
EXPOSE 80
EXPOSE 2000/udp
EXPOSE 2000/tcp
CMD ["sh", "-c", "xray-daemon -f /var/log/xray-daemon.log -t 0.0.0.0:2000 -b 0.0.0.0:2000 &; java -jar /opt/app/blog-0.0.1-SNAPSHOT.jar"]
