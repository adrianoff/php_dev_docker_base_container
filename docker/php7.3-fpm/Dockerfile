FROM phpdockerio/php73-fpm:latest

RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.3-mysql php-redis php7.3-dev php7.3-sqlite3 php7.3-bcmath php7.3-soap php7.3-bz2 php7.3-gd php-imagick php7.3-intl php7.3-mbstring php7.3-xsl php7.3-tidy php7.3-xmlrpc php-yaml \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN apt-get update \
        && apt-get -y --no-install-recommends install php-xdebug \
        && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/* \

RUN apt-get update && apt-get install -y \
    git \
    unzip \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer --version

WORKDIR "/var/www/temp"
