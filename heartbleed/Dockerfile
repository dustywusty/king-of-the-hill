FROM ubuntu:12.04
MAINTAINER Dustin Clark "dusty@isperldead.net"

#
# ..
# --------------------------------------------------------- #

RUN \ 
  apt-get update && \
  apt-get install -y build-essential curl nginx openssl && \
  rm -rf /var/lib/apt/lists/* && \
  echo "\ndaemon off;" >> /etc/nginx/nginx.conf && \
  chown -R www-data:www-data /var/lib/nginx

#
#
# --------------------------------------------------------- #

VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/ssl", "/var/log/nginx", "/usr/share/nginx/www"]

#
# ..
# --------------------------------------------------------- #

CMD ["nginx"]
