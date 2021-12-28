# docker-wordpress-local-dev
Build a local development environment for Wordpress using docker.

### To get start from nothing...
in a terminal (bash shell)
```cd ~/projects
git clone https://github.com/jsidberry/docker-wordpress-local-dev.git
cd docker-wordpress-local-dev
docker-compose up -d
```

### After running compose...
in a browser, type `http://localhost:8000`
this will bring up the initial Wordpress 5-minute easy setup start page.
- select `English`
- admin username is `admin`
- admin password is `password`
- admin email is `test@test.com`

### To delete the entire dev environment
in a terminal (bash shell)

goto the projects directory `cd ~/projects/`

list the running docker containers `docker ps`

stop the frontend wordpress site `docker stop {container-id}`

stop the phpMyAdmin from running `docker stop {container-id}`

stop the MySQL database from running `docker stop {container-id}`

list the containers for the site `docker ps -a`

remove the three (3) containers related to the project `docker rm {container-id} {container-id} {container-id}`

find the persistent volume created by the database `docker volume ls`

remove the volume associated with the wordpress dev environment: `docker volume rm {docker-wordpress-local-dev_db_data}`
