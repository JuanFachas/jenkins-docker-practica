FROM php:8.1-apache

# Activar módulo rewrite
RUN a2enmod rewrite

# Instalar extensiones y utilidades necesarias
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
    xmlrpc \
    soap \
    opcache

# Configurar el timezone si quieres
# RUN echo "date.timezone = America/Bogota" > /usr/local/etc/php/conf.d/timezone.ini

# Copia los archivos de la app (si tienes una app)
# COPY . /var/www/html

# Dar permisos adecuados (si es necesario)
# RUN chown -R www-data:www-data /var/www/html

# Exponer el puerto (aunque Apache ya expone el 80)
EXPOSE 80
