```shell
VERSION=2.20.2
docker build --build-arg IMAGE_VERSION=8-jre8 --build-arg GS_VERSION=2.20.2 -t kartoza/geoserver:${VERSION} .

9.0-jdk8-openjdk-slim-buster

docker build -t kartoza/geoserver:${VERSION} .

https://liquidtelecom.dl.sourceforge.net/project/geoserver/GeoServer/2.20.2/extensions/geoserver-2.20.2-mongodb-plugin.zip
https://build.geoserver.org/geoserver/2.20.x/community-latest/geoserver-2.20-SNAPSHOT-activeMQ-broker-plugin.zip
```

```
https://build.geoserver.org/
jenkins
```