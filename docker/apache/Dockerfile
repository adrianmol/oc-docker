# docker/apache/Dockerfile
FROM httpd:2.4.51

COPY default.apache.conf /usr/local/apache2/conf/default.apache.conf

RUN echo "Include /usr/local/apache2/conf/default.apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf