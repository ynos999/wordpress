# wordpress

docker-compose file with 4 wordpress, 4 databases and local docker network.

## How To Setup

```
mkdir -p /home/MyUser/app
cd /home/MyUser/app
git clone 

cp docker-compose.yml /home/MyUser/app

cp .env /home/MyUser/app

cd /home/MyUser/app

docker-compose up -d
```

```
#View dockers
sudo docker ps -a
```

```
#Remove docker
sudo docker rm
```

```
# Docker compose up
sudo docker-compose up -d
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
#Delete all inactive dockers

sudo docker rm -f $(sudo docker ps -a -q)
```

```
# Delete all docker images
sudo docker rmi -f $(sudo docker images -q)
```

```
# Start docker-compose

sudo docker-compose up -d
```

```
# 

sudo docker image prune -a
```

```
# 

sudo docker-compose -f docker-compose.yml logs -f
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
