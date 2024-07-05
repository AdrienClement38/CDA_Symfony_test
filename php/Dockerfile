# Utilise l'image officielle PHP 8.2 FPM
FROM php:8.2-fpm

# Mise à jour des paquets et installation de git et unzip, nécessaires pour Composer
RUN apt-get update && apt-get install -y git unzip

# Téléchargement et installation de Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Définit le répertoire de travail
WORKDIR /var/www/html

# Copie l'application dans le conteneur
COPY . /var/www/html
