FROM nextcloud:apache

RUN apt-get -qq update && apt-get -qq install -y \
    supervisor  < /dev/null > /dev/null \
  && rm -rf /var/lib/apt/lists/* \
  && mkdir /var/log/supervisord /var/run/supervisord

COPY supervisord.conf /etc/supervisor/supervisord.conf

ENV NEXTCLOUD_UPDATE=1

CMD ["/usr/bin/supervisord"]
