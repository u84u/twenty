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

to run the app in multiworkspace mode, do not add any new env vars before the first signup. after you signup the first time, you will now have access to the admin panel in settings.
in there change `IS_MULTIWORKSPACE_ENABLED` to true and save changes. now the create workspace button on top right should work. the `DEFAULT_SUBDOMAIN` is `app` so while in localhost, the signup page goes to `app.localhost`.
maybe look more into how `PUBLIC_DOMAIN_URL` works.
