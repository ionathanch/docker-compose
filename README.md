# Template

```yaml
version: "3"

services:
  example:
    image: author/example:tag
    container_name: example
    restart: always
    environment:
      - ENV_VAR=value
    ports:
      - 8000:80
    volumes:
      - /unnamed/volume/will/be/created
      - myvolume:/var/www/html
      - /srv/data/host/location:/srv/data
    networks:
      - mynetwork
    depends_on:
      - db
  db:
    image: postgres
    container_name: example-db
    restart: always
    expose:
      - 5432
    volumes:
      - example-db:/var/lib/postgresql/9.3./main
      
networks:
  mynetwork:

volumes:
  myvolume:
  example-db:

```
