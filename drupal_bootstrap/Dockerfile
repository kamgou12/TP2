# Utilise l'image Drupal 9
FROM drupal:9

# Installe git et nettoye après l'installation
RUN apt update && apt install -y git && rm -rf /var/lib/apt/lists/*

# Change  le répertoire de travail pour le dossier des thèmes
WORKDIR /var/www/html/themes

# Cloner le thème Bootstrap depuis le dépôt officiel de Drupal
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

# Retour au répertoire principal de Drupal
WORKDIR /var/www/html
