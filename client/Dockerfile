FROM httpd:2.4.48
RUN apt update && \
    apt install apt-utils build-essential systemd net-tools locales git zip unzip nano -y

RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

RUN passwd -d www

COPY --chown=www:www . /usr/local/apache2/htdocs/
WORKDIR /usr/local/apache2/htdocs/

EXPOSE 80