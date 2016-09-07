# LetsEncrypt-docker

Simple LetsEncrypt implementation on Ubuntu 16.04 LTS

## Command line
```
docker run -it --rm -p 80:80 -p 443:443 -v /local/letsencrypt:/etc/letsencrypt wark/letsencrypt bash
```

## Add certificates
To subdirectory named after first domain
```
letsencrypt certonly --standalone -d example.com -d www.example.com \
    --noninteractive --agree-tos --email contact@example.com
```

Certificates can be found in `/etc/letsencrypt/live` (in above example `/docker/letsencrypt/live`)

## Reneval expiring certificates
```
letsencrypt certonly --standalone renew \
    --noninteractive --agree-tos --email contact@example.com
```
