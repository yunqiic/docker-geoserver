```
VERSION=2.20.2
docker build --build-arg IMAGE_VERSION=8-jre8 --build-arg GS_VERSION=2.20.2 -t kartoza/geoserver:${VERSION} .
```