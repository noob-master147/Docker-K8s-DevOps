# This project demonstrate the use of docker to deploy multiple container application

## Architecture
![Architecture](./images/p1.png) 

<br>
<br>

## Flow of the Application
![Flow](./images/p2.png)


<br>
<br>

# Step 1
## Make DEV Dockerfiles of
    *   React App
    *   Express Server
    *   Worker environment

- We dont want to rebuilt the images upon changes while devlopment
![Flow](./images/p3.png)

<br>
<br>


# Step 2
## Docker  Compose 
![Flow](./images/p4.png)


<br>
<br>

# Step 3
## Envrionment Varibles
![Flow](./images/p5.png)


<br>
<br>

- NOTE
    - We do not have port mapping in docker-compose.yml
    - There are 2 Servers
        - Express
        - React

### The Nginx server will get all the req, and decide which backend service to route to.
![Nginx Server Flow](./images/p6.png)

<br>
<br>

# Step 4
## Configure NginX Server

<br>

![Flow](./images/p7.png)

<br>

- we will make a conter for nginx server
- Include and configure the nginx service in the docker-compose.yml
- ```sudo docker-compose up --build```
- The React app will be available att localhost:3050

<br>
<br>

# Step 5
## Open WebSockets

<br>

![Flow](./images/p8.png)

### To open Web Socket, add this in nginx default.config file

    location /sockjs-node {
        proxy_pass http://client;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "Upgrade";
    }