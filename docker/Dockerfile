# 基础镜像，基于openjdk:8-jre操作系统
FROM openjdk:8-jre
# 维护人员信息
MAINTAINER PeterZhang "1097692918@qq.com"

RUN sed -i s/deb.debian.org/mirrors.aliyun.com/g /etc/apt/sources.list

RUN apt-get -y update; apt-get -y --no-install-recommends install fonts-cantarell lmodern ttf-aenigma \
    ttf-bitstream-vera ttf-sjfonts tv-fonts  libapr1-dev libssl-dev  \
    gdal-bin wget zip unzip curl xsltproc certbot  cabextract gettext postgresql-client figlet

RUN set -e \
    export DEBIAN_FRONTEND=noninteractive \
    dpkg-divert --local --rename --add /sbin/initctl \
    && (echo "Yes, do as I say!" | apt-get remove --force-yes login) \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \

# 移动geoserver文件夹到/usr/local/geoserver 下
ADD geoserver /usr/local/geoserver
# 配置环境变量
ENV GEOSERVER_HOME /usr/local/geoserver
# 暴露8011端口
EXPOSE 8011
# 设置镜像启动时执行的命令
