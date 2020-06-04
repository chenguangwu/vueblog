# Docker image for springboot file run
# VERSION 0.0.1
# Author: cgw
# 基础镜像使用java
FROM java:8
#时区设置
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo 'Asia/Shanghai' >/etc/timezone

# 作者
MAINTAINER cgw

# 将jar包添加到容器中并更名为app.jar
ADD /target/vueblog-0.0.1-SNAPSHOT.jar /home/app.jar

# 运行jar包
RUN bash -c 'touch /home/app.jar'
ENTRYPOINT  java ${JAVA_OPTS}  -jar /home/app.jar

#docker run -d --name vueblog -p 8081:8081 -e JAVA_OPTS=-Dspring.profiles.active=docker vueblog