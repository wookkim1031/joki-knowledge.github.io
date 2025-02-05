# Docker 

## What is Docker? 

Process of Developing, Deploying, and running applications using containerization. 

## Containers

- Lightweight, isolated environments that package an application and its dependencies. Unlike VMs containers share the host OS kernel. 
- Sharing possible while programming together with friends 


## Images

Read only templates used to create containers. Images built from Dockerfiles. 

## Docker Engine

- Core Component includes: 

1. Daemon : Manages containers, images, networks and volumes
2. REST API: Allows interaction with the daemon.
3. CLI: Commmand-line interface for users 

## Registries

Repositories for storing and sharing images. Docker Hub is the default public registry (e.g. official images for Node.js, PostgreSQL)
while private registries host custom images. 

## Docker compose 

A tool for defining and managing multi-container applications via a docker-compose.yml file.

# Usage of Docker

npm install 

### Create a Dockerfile

 FROM node:14
    
 WORKDIR /app
    
 COPY package.json .
    
 RUN npm install
    
 COPY . .
    
 EXPOSE 3000
    
 CMD [ "node", "app.mjs" ]

 ### Create Docker image 

 docker build .

### Run Docker

docker run -p 3000:3000 2f04e8cfc9b0f969798e302ce4b9616354c059191a5fbd2d0f68cf4c410ec79c

### Check if the Docker is working 

http://localhost:3000/

### Stop Docker from running 

docker stop brave_newton

