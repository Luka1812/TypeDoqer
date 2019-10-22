# TypeDoqer
Laravel docker for local development.

Instructions for setting up TypeDoqer.

### 1. Pull TypeDoqer in your project's root directory
### 2. Make changes on your typedoqer's env file 
- check docker.env file in TypeDoqer directory
- inside of docker.env file set name of your local database

### 3. Make changes on your project's env file 
DB_CONNECTION=mysql
DB_HOST=mysql

### 4. Create your own sites-available config file
- go to TypeDoqer/nginx/sites-available and cp default.conf
- change this => server_name www.your_custom-domain.extension your_custom-domain.extension;
- update your local machine's /etc/hosts file and register above domains in it

### 5. Set your project name/name of root directory
- go to TypeDoqer/.docker.env and change PROJECT_NAME var

### 6. Run docker
- go to TypeDoqer directory and run following commands:

`docker-compose build` 

`docker-compose up -d` 

### 6. Enter in your workspace 
`docker exec -it typedoqer_app_1 bash` 
- where you can run commands such as composer, npm and so on