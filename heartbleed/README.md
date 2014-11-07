```
docker run -d -p 80:80 -p 443:443 -v /var/docker/heartbleed/etc/nginx/sites-enabled:/etc/nginx/sites-enabled -v /var/docker/heartbleed/etc/nginx/certs:/etc/nginx/certs -v /var/docker/heartbleed/var/log/nginx:/var/log/nginx heartbleed
```
