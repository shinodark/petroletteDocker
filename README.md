# petroletteDocker

This project aims to build petrolette software in a docker environment, ready to use for self-hosting. 
Initial projet on https://github.com/philtreF/petroletteDocker

## Tools used
 - Docker
 - Docker-compose
 - Traefik reverse proxy with let's encrypt SSL

## Steps to build an environment
1. Create a .env file and set variable environments for domain and email, and traefik dashboard authentication :
    
		DOMAIN=example.com
		EMAIL=mail@example.com
		TRAEFIK_USER=admin
		TRAEFIK_PASSWORD_HASH=$$blablablablablablablabla

2. run `docker build -t petrolette .`
3. run `docker-compose up -d`
4. Read news using this wonderful tool. 

## Already got a reverse proxy ?
This docker container can be run without traefik if you already got a reverse-proxy

## Credits

- Software Repository: https://framagit.org/yphil/petrolette (consider donating)
