
```
	docker run -d --name heartbleed \
		-p 80:80 \
		-p 443:443 \
		-v /var/docker/heartbleed/etc/nginx/sites-enabled:/etc/nginx/sites-enabled \
		-v /var/docker/heartbleed/etc/nginx/ssl:/etc/nginx/ssl \
		-v /var/docker/heartbleed/var/log/nginx:/var/log/nginx \
		-v /var/docker/heartbleed/usr/share/nginx/www:/usr/share/nginx/www \
		hackhuntsville/heartbleed:latest
```

```
openssl req \
    -new \
    -newkey rsa:4096 \
    -days 365 \
    -nodes \
    -x509 \
    -subj "/C=US/ST=Denial/L=Springfield/O=Dis/CN=107.22.8.84" \
    -keyout server.key \
    -out server.crt

```
