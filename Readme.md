# Symfony-docker

### Why did I make this?
I was hosting some api's on my server for an app that I made and used Apache reverse proxy to route everything. But i wanted to change things around and use Traefik for routing/proxy. Most of the things I use on my server are docker containers anyway. 

But then came the problem that I could not get my local sites working in Traefik, so that is why I wanted to make some containers to handle this.

### What does it do?
The docker-compose script makes 2 containers. One for PHP and one for NGINX. I didn't want one for MySQL because I'm running that on my docker host and have some script to make backups regularly.

### What do I need to do to use this?
Just clone this repo in a new folder of your existing Symfony project and use "docker-compose up -d" to run everything and just wait :)

Take a look in the docker-compose.yaml if you want to make some changes like ports if you need to. I use port 8888 for accessing the site, but you can change that if you want. If you want to use it with traefik like I do, uncomment the lines and change "DOMAINNAME" and "BACKENDNAME" to what you need it to be.

