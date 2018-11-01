FROM drupal:8.6

RUN apt-get update && apt-get install -y git \
    apt-get purge -y --AutoRemove -o APT::AutoRemove:RecommendsImportant=false; \
    rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

WORKDIR /var/www/html






