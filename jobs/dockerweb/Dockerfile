# Imagen base de PHP 8.1 con Apache
FROM php:8.1-apache

# Habilita el módulo rewrite de Apache
RUN a2enmod rewrite

# Actualiza paquetes e instala dependencias necesarias
RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libicu-dev \
    libxml2-dev \
    libpq-dev \
    unzip \
    git \
    vim \
    && docker-php-ext-install \
    pdo \
    pdo_mysql \
    pdo_pgsql \
    zip \
    intl \
    soap \
    opcache

# Copia el contenido del proyecto al directorio de Apache
COPY . /var/www/html/

# Establece los permisos adecuados (opcional)
RUN chown -R www-data:www-data /var/www/html
