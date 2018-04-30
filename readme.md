# Docker LEMP Stack

LEMP ( Linux, NGINX, MariaDB and PHP ) is one of common stack for building web application. This container includes all basic functionality to get your website up and running quickly.

## Directory Structure

```
.
├── app                 # All of your php file should be placed here, treat it like /var/www directory
│   └── index.php       # Default index file
├── database            # The database is saved here
├── nginx               # This folder contains nginx specified configuration
│   └── default.conf    # Default configuration file
├── php                 # Contains custom PHP7-fpm docker configuration
│   └── Dockerfile      # Docker configuration file for PHP container
├── docker-compose.yml  # Docker configuration for this project
└── readme.md           # Description for this project
```

## Documentation

### Requirements

You should make sure that `docker` and `docker-compose` command has been installed. Take a look this tutorial to install them,

- Docker: [https://docs.docker.com/install/linux/docker-ce/ubuntu/](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- Docker Compose: [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)

### Steps

1. Clone or download this repository
2. Navigate your terminal prompt to that folder
3. Execute this command to fetch the container dependencies image if You never use Docker before then run it locally

`docker-compose -d up`

4. Access
   - `localhost:8080` is used for serving the webserver.
   - `localhost:8000` to access phpMyAdmin

   Credentials for phpMyAdmin
   Server: mariadb
   Username: root
   Password: admin123