FROM php:7.4-fpm

RUN apt-get update
# RUN apt-get install -y
RUN apt-get install -y zip
RUN apt-get install -y unzip
RUN apt-get install -y git 
RUN apt-get install -y curl 
    # mysqli \
    # && docker-php-ext-install mysqli
    
# Install MySQLi
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Install PDO
RUN docker-php-ext-install pdo_mysql

# Composer installing
RUN curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/ \
    && ln -s /usr/local/bin/composer.phar /usr/local/bin/composer

# Install composer
# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www