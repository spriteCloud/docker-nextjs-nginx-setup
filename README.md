# Nextjs and nginx in docker setup

## Summary of the setup
- docker-compose.yml describes the setup amd the containers that are launched
- Nginx has a self signed certificate for localhost. Replace this with your own wildcard cert and you can access the setup over https with any subdomain of your choice.
- Only nginx accepts external https connections and forwards them to the nextjs container.
- Within the docker network, nextjs can be accessed at nextjs:8080
- Within the docker network, mysql can be accessed at mysql:3306
- mysql container is also launched, but not used yet

## Installation
- have a linux distribution
- install docker
- Get this repo

## Running the containers
Start with the command
```
docker-compose up -d
```

Now the web app can be reached at
```
https://localhost
```

Stop with the command
```
docker-compose down
```
