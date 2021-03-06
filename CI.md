# Notes for Continuous Integration Workflow for Multiple Images
## Deployment for The React Fib project

<br>
<br>

## Step1
### Multi Container Setup
![Flow](./images/p9.png)

**How this setup is different from thr previous is that this time Travis CI will build the production images and publish it on DockerHub. Amazon EB will pull these images from the DockerHub and then deploy.**

<br>
<br>

## Step2
### Setup Prod Docker Files for Server and Client
![Flow](./images/c1.png)

<br>
<br>

## Step3
### Set up Travis CI
**This is working involded around TravisCI**
![Travis Flow](./images/c2.png)

<br>
<br>

## Step4
### Configure Amazon EB for Multiple Cont

**[Amazon Elastic Container Service](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)**
![Amazon EB](./images/c4.png)

<br>

**Add Dockerrun.aws.json file**
![Amazon EB](./images/c3.png)

<br>

**Links**
![Links](./images/c5.png)


<br>
<br>

# Production Architecture
![Production](./images/c6.png)

## AWS Elastic Cache
![AWS Elastic Cache](./images/c7.png)