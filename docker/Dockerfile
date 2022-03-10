# 基础镜像，基于openjdk:8-jre-alpine操作系统
FROM openjdk:8-jre-alpine
# 维护人员信息
MAINTAINER PeterZhang "1097692918@qq.com"
# 移动geoserver文件夹到/usr/local/geoserver 下
ADD geoserver /usr/local/geoserver
# 配置环境变量
ENV GEOSERVER_HOME /usr/local/geoserver
# 暴露8011端口
EXPOSE 8011
# 设置镜像启动时执行的命令
ENTRYPOINT ["sh","/usr/local/geoserver/bin/startup.sh"]