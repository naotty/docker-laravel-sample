FROM tnaototo/php-base:1.0
MAINTAINER tnaototo

USER root
WORKDIR /root


# Apache設定
COPY config/httpd.conf /etc/httpd/conf/httpd.conf


WORKDIR /var/www/html

# Laravel
RUN git clone https://github.com/naotty/laravel-sample-app.git /var/www/html
RUN git checkout 3fd269b9f3569d202bd61e970cd8586033e33f09

RUN /usr/local/bin/composer.phar install

RUN chown apache:apache -R /var/www/html/
RUN chmod 777 -R /var/www/html/storage
