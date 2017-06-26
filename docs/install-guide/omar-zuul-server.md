# OMAR Zuul Server

## Dockerfile
```
FROM omar-base
RUN mkdir /usr/share/omar
COPY omar-zuul-server-1.0.0-SNAPSHOT.jar /usr/share/omar
USER 1001
WORKDIR /usr/share/omar
VOLUME /dev/random /home /Users
EXPOSE 8761
CMD java -Xms256m -Xmx1024m -Dspring.profiles.active=production -Djava.security.egd=file:/dev/./urandom -Dserver.contextPath=/omar-zuul-server -jar /usr/share/omar/omar-zuul-server-1.0.0-SNAPSHOT.jar
```
Ref: [omar-base](../../../omar-base/docs/install-guide/omar-ossim-base/)

## JAR
`http://artifacts.radiantbluecloud.com/artifactory/webapp/#/artifacts/browse/tree/General/omar-local/io/ossim/omar/apps/omar-zuul-server`
