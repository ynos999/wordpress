# wordpress - docker-compose.yml file with 4 wordpress, 4 databases and local docker network.

## How To Setup - Ubuntu 22.04

Before start project you need install docker and docker compose.

Please, in .env file change database names and passwords, before use command sudo docker-compose up -d...

```
sudo apt update -y

sudo apt install git -y

mkdir -p /home/MyUser/app

cd /home/MyUser/app

git clone https://github.com/ynos999/wordpress

cd /home/MyUser/app/wordpress

cp docker-compose.yml /home/MyUser/app

cp .env /home/MyUser/app

cd ..

rm /home/MyUser/app/wordpress

# Docker compose up
sudo docker-compose up -d
```

```
#View dockers

sudo docker ps -a
```

```
#Remove docker example

sudo docker rm wp1
```

```
# Login in docker

sudo docker exec -i -t wp1 bash
```

```
# Stop dockers

sudo docker-compose stop
```
```
# Delete docker-compose dockers

sudo docker-compose down
```

```
#Delete all inactive dockers

sudo docker rm -f $(sudo docker ps -a -q)
```

```
# Delete all docker images

sudo docker rmi -f $(sudo docker images -q)
```

```
# Docker volumes

sudo docker volume ls
```

```
#Copy files from docker

docker cp wp1:/var/www /var/www/
```

```
#Autostart all dockers after server reboot

sudo docker update --restart unless-stopped $(sudo docker ps -q)
```
