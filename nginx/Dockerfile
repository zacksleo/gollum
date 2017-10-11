FROM nginx:1.7.10
COPY nginx.conf /etc/nginx/nginx.conf
COPY ssl-cert/ssl.key /etc/nginx/ssl-cert/ssl.key
COPY ssl-cert/ssl.crt /etc/nginx/ssl-cert/ssl.crt

RUN apt-get -y update && apt-get -y install wget
RUN wget http://7s1rjx.com1.z0.glb.clouddn.com/oauth2_proxy -O /usr/local/bin/oauth2_proxy
#COPY oauth2_proxy /usr/local/bin/oauth2_proxy
RUN chmod +x  /usr/local/bin/oauth2_proxy
