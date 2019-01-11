### Start containers

```bash
docker-compose up -d
```

### Using

For using php container(composer install, symfony cli, etc):

```bash
docker-compose exec adrianoff_php_service bash
```

or run command

```bash
cd docker
docker-compose exec adrianoff_php_service bash -c "composer install"