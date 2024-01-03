# Wordpress Local Development Setup with Docker Compose

## Prerequisites
Make sure you have Git, Docker installed before you run the script! Also make sure no other Docker containers are currently running.

## Set your Domain name
```
nginx > confi.d > nginx.conf
```
Line 3
```
server_name xxx.xx.com;
```

## Set up Database
```
open docker-compose.yml
```

Line 30 to 34
Change databse name, username and password

```
MYSQL_ROOT_PASSWORD: xxxx
MYSQL_DATABASE: xxxx
MYSQL_USER: xxxxx
MYSQL_PASSWORD: xxxx
```

## How to run

Check other docker containter whether running or not before you run docker-compose up.

```
$ docker ps
```

If running, stop any running containers
```
$ docker stop $(docker ps -aq)
```

Run script
```
- $ docker-compose up -d
```

### Add domain name on hosts file

```
127.0.0.1 xxx.xx.com
```
