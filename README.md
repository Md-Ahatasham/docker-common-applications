# install laravel without composer on docker


docker run --rm --interactive --tty \
--volume $PWD:/app \
--volume ${COMPOSER_HOME:$HOME/.composer}:/tmp \
composer create-project laravel/laravel practice