minimum steps required to self host [twenty](https://github.com/twentyhq/twenty).

```shell
$ curl -o .env https://raw.githubusercontent.com/twentyhq/twenty/refs/heads/main/packages/twenty-docker/.env.example
$ openssl rand -base64 32
$ # replace APP_SECRET with the above command's output in .env
$ # setup a strong PG_DATABASE_PASSWORD in .env
$ curl -o docker-compose.yml https://raw.githubusercontent.com/twentyhq/twenty/refs/heads/main/packages/twenty-docker/docker-compose.yml
$ docker compose up -d
```

this assumes you have both openssl and docker command line installed.
