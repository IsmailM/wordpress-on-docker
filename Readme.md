# Wordpress on Docker
This setup uses two interconnected docker images - one for wordpress and one for mariadb (mysql). Both of these dockers are linked to folders within this repo to ensure the data is persistant.

## Running WordPress
After starting the Docker Daemon:

```bash
docker-compose up
```

Then open [http://localhost:8080/](http://localhost:8080/) in your favourite browser!

## Database
It's easier to push the db as a tar.gz - so I normally tar my db folder every now and then push it to github...

## Wordpress to static site
After install httrack, in a new terminal (i.e. with docker running):
```bash
httrack --clean -O _site http://localhost:8080
```

And the static website will output to `_site/localhost_8080`.

## PRs Welcome...
Any suggestions welcome.
