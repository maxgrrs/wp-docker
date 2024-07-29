# wp-docker
wordpress setup based on docker compose

1. clone repository
2. cp .env-example to .env and fill in credentials of your choice
3. get a domain, install certbot (for 'web hosting product' on 'debian 10') and request certificates for your domains
4. cd to nginx/conf/ and cp default.conf-example to default.conf 
5. replace yourdomain.com in default.conf by your domain
6. install docker, docker compose up at compose file and done

To set up automatic certificate renewal use:
```shell
sudo certbot certonly --webroot --webroot-path=/var/lib/docker/volumes/wp-docker_webroot/_data --config-dir /var/lib/docker/volumes/wp-docker_certbot_data/_data --email [your email] --agree-tos --no-eff-email --renew-by-default -d [your domain]
```
