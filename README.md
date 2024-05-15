# clone the project
# cd project name
## steps to run the project ##
1. create .env file from .env.example
2. create docker-compose.override.yml from  docker-compose.override.example.yml
3. create docker-compose.override.mysql.yml from  docker-compose.override.mysql.example.yml
4. create docker-compose.override.redis.yml from  docker-compose.override.redis.example.yml
5. create docker-compose.override.adminer.yml from  docker-compose.override.adminer.example.yml

# run docker compose or (docker-compose based on your setup) up -d 
## that's it. now you can use database like phpmyadmin in browser  like: http://localhost:8080
## you can now connect db using username: 'root' and pass 'secret'
## you can now connect redis using password 'secret'
## you will find the necessary port in respective .env file within .envs folder




# install laravel without composer on docker

docker run --rm --interactive --tty \
--volume $PWD:/app \
--volume ${COMPOSER_HOME:$HOME/.composer}:/tmp \
composer create-project laravel/laravel practice