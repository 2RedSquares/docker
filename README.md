# General Docker Commands

 * [Limit a Container's Resources](https://docs.docker.com/config/containers/resource_constraints/)

# Docker Command Reference

## Push to Docker Hub

    docker push <tag>

# Portainer

[Portainer](https://portainer.io/) is an open source, lightweight management user interface which allows you to easily manage your local docker hosts or swarm clusters.

## Deployment

### One time setup for data volume

    docker volume create portainer_data

### Execute Image

    docker run -d --name=portainer -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer


## Get Latest

    docker pull portainer/portainer:latest

##

# Miscellaneous

## Start TOMCAT with WAR

    docker run -it -p 8080:8080 -v $(pwd)/demo-0.0.1-SNAPSHOT.war:/usr/local/tomcat/webapps/demo.war tomcat:8.0.33
