FROM ubuntu:12.04
MAINTAINER Dustin Clark "dusty@isperldead.net"

#
# Install a vulrenable version of openssl
# --------------------------------------------------------- #

RUN \
  apt-get update && \
  apt-get install -y wget && \
  wget -P /tmp/ http://launchpadlibrarian.net/141622187/libssl1.0.0_1.0.1-4ubuntu5.10_amd64.deb && \
  wget -P /tmp/ http://launchpadlibrarian.net/141622186/openssl_1.0.1-4ubuntu5.10_amd64.deb && \
  dpkg -i /tmp/libssl1.0.0_1.0.1-4ubuntu5.10_amd64.deb && \
  dpkg -i /tmp/openssl_1.0.1-4ubuntu5.10_amd64.deb

#
# Install nginx
# --------------------------------------------------------- #

RUN \ 
  apt-get install -y nginx && \
  echo "\ndaemon off;" >> /etc/nginx/nginx.conf && \
  chown -R www-data:www-data /var/lib/nginx

#
# Volumes
# --------------------------------------------------------- #

VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/ssl", "/var/log/nginx", "/usr/share/nginx/www"]

#
# ..
# --------------------------------------------------------- #

CMD ["nginx"]
