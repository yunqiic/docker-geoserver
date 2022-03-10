```shell

# 解压到指定目录
unzip geoserver-2.11.0-bin.zip -d docker-geoserver/
 
# 重命名
mv geoserver-2.11.0 geoserver
 
# 修改geoserver的监听端口，默认8080，防止冲突
# cd 到geoserver目录下,修改start.ini中的监听port为9090.保存退出

docker build -t holly/geoserver .

# 可以看到刚生成的geoserver镜像
docker images
# 执行geoserver镜像
docker run -d --name geoserver -p 8011:8011 holly/geoserver 
 
docker run -d --name geoserver -p 8080:8080  -v /root/geoserver/data_dir:/usr/local/geoserver/data_dir geoserver 
# 查看geoserver镜像是否运行
docker ps
```