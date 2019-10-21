# TypeDoqer
Laravel docker for local development.

Instructions for setting up TypeDoqer.

### 1. Pull TypeDoqer in your project's root directory
### 2. Make changes on your project's env file 
- check docker.env file in TypeDoqer dir
- inside of docker.env file set name of your local database

DB_CONNECTION=mysql

DB_HOST=mysql

DB_PORT=database_port_should_be_the_same_as_from_docker_env

DB_DATABASE=database_name_should_be_the_same_as_from_docker_env

DB_USERNAME=database_username_should_be_the_same_as_from_docker_env

DB_PASSWORD=database_password_should_be_the_same_as_from_docker_env

### 3. Create your own sites-available config file
- go to TypeDoqer/nginx/sites-available and cp default.conf
- change this => server_name www.your_custom-domain.extension your_custom-domain.extension;
- update your local machine's /etc/hosts file and register above domains in it

### 3. Set your project name/name of root directory
- go to TypeDoqer/.docker.env and change PROJECT_NAME var