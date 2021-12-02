    FROM centos:8
     
    ENV TZ=Europe/Moscow
     
    RUN yum update -y && yum install -y nginx php php-fpm php-mysqli php-xml php-json && clean all
    RUN echo "daemon off;" >> /etc/nginx/nginx.conf
    RUN mkdir /run/php-fpm
     
    COPY ./html/ /usr/share/nginx/html/
     
    CMD php-fpm -D ; nginx
     
    EXPOSE 80

