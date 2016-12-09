FROM webdevops/apache:ubuntu-16.04

MAINTAINER Eric Pfeiffer <computerfr33k@users.noreply.github.com>

ARG PHP_SOCKET=php-fpm:9000

ENV WEB_PHP_SOCKET=$PHP_SOCKET

#ENV WEB_DOCUMENT_ROOT=/var/www/public
ENV WEB_DOCUMENT_ROOT=/var/www/help

EXPOSE 80 443

#WORKDIR /var/www/public
WORKDIR /var/www/help

ENTRYPOINT ["/opt/docker/bin/entrypoint.sh"]

RUN a2enmod rewrite
#RUN a2ensite test-dev.conf
RUN service apache2 restart

CMD ["supervisord"]
