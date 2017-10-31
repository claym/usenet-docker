# Usenet Docker

This repo is my version of another fork. Setup should be a bit easier but even the original was pretty straightforward.

## Containers

* [jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy) - Nginx Proxy 
* [linuxserver/sonarr](https://github.com/linuxserver/docker-sonarr) - Sonarr 
* [linuxserver/plexpy](https://github.com/linuxserver/docker-plexpy) - Plexpy 
* [linuxserver/hydra](https://github.com/linuxserver/docker-hydra) - NZBHydra 
* [linuxserver/muximux](https://github.com/linuxserver/docker-muximux) - Muximux 
* [linuxserver/radarr](https://github.com/linuxserver/docker-radarr) - Radarr 
* [linuxserver/ombi](https://github.com/linuxserver/docker-ombi) - Ombi 
* [linuxserver/nzbget](https://github.com/linuxserver/docker-nzbget) - NZBGet 
* [linuxserver/nzbget](https://github.com/linuxserver/docker-ubooquity) - Ubooquity
* [linuxserver/nzbget](https://github.com/linuxserver/docker-mylar) - Mylar


## Docker Setup
1. Update `./uidgid.env` with the user and group IDs that will be running Docker
2. Update `./.env` and add your own Hostname as well as your directory for config, downloads, movies and TV folders
3. Create the necessary folders and make sure the user/group running the containers is the same
3. Choose which services containers to use and remove the extras from the `./docker-compose.yml` file
4. Run `docker-compose up -d` to start all the Usenet services

### Note about Plex and setting up Plex server
* Initially when all containers are fully running, Plex is accessible by IP:PORT/web/index.html but the Plex Server configuration is hidden.  This is due to the Plex container being behind the Docker Network's IP and not being able to connect to Plex.tv
* Basically from as stated in the original repo you need to tunnel the container and access the page. In order to do so follow the instructions on https://support.plex.tv/hc/en-us/articles/200288586-Installation specifically the section on "Opening the Plex Web App on a Device Other than the Server Itself"

### Services setup
* The htpc guides are pretty nifty: https://www.htpcguides.com
