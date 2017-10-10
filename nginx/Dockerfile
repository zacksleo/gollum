FROM nginx:1.7.10
COPY nginx.conf /etc/nginx/nginx.conf
COPY ssl-cert/ssl.key /etc/nginx/ssl-cert/ssl.key
COPY ssl-cert/ssl.crt /etc/nginx/ssl-cert/ssl.crt
RUN cat > /etc/apt/sources.list << END \
deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse \n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse \n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse \n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse \n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse \n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse \n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse \n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse \n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse \n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse \n\
END
RUN apt-get update && RUN apt-get install wget
RUN wget http://7s1rjx.com1.z0.glb.clouddn.com/oauth2_proxy -O /usr/local/bin/oauth2_proxy
