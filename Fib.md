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

