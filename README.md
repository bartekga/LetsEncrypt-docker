# LetsEncrypt-docker

Simple LetsEncrypt implementation on Ubuntu 16.04 LTS

```
docker run -it --rm -p 80:80 -p 443:443 -v /docker/letsencrypt:/etc/letsencrypt wark/letsencrypt bash
```

```
letsencrypt certonly --standalone -d example.com -d www.example.com \
    --noninteractive --agree-tos --email contact@example.com
```

Certificates can be found in `/etc/letsencrypt/live` (in above example `/docker/letsencrypt/live`)

