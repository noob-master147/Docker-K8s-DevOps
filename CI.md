# Notes for Continuous Integration Workflow for Multiple Images
## Deployment for The React Fib project

<br>
<br>

## Step1
### Multi Container Setup
![Flow](./images/p9.png)

How this setup is different from thr previous is that this time Travis CI will build the production images and publish it on DockerHub. Amazon EB will pull these images from the DockerHub and then deploy.

<br>
<br>

## Step2
### Setup Prod Docker Files for Server and Client
![Flow](./images/c1.png)
<br>
<br>

## Step3
### Set up Travis CI to GitHub Repository

<br>
<br>

## Step4
###