FROM nginx:1.9
MAINTAINER mapk0y@gmail.com

COPY rocketchat.conf /etc/nginx/conf.d/
# for docker logs
RUN ln -snvf /dev/stdout /var/log/nginx/proxy.access.log
