
# AWS 3 Tier Web Architecture

Hosting a 3 tier Web Application in AWS 

### Architecture Overview

![3TierArch](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/fd09b3f6-f07f-487c-ba5d-2f9a038a7ef8)

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.


### VPC and Networking Configuration :
![Screenshot (223)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/126942ce-60fd-496c-a6d3-0fcfca55dc84)

 we will build the VPC networking components and security groups to enhance the security of our infrastructure, including EC2 instances, Aurora databases, and Elastic Load Balancers.

Creating an isolated network with the following components:<br/>

* VPC  <br/>
* Subnets  <br/>
* Route Tables  <br/>
* Internet Gateway  <br/>
* NAT Gateway  <br/>
* Security Groups  <br/>

### creating S3 Bucket and uploading the files
![Screenshot (227)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/2618b914-b758-4aed-ad12-d0157e64f75a)

### RDS Configuration :
![Screenshot (224)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/895f1519-f0e2-453c-9e0f-7eb4f71d521b)

In this section of our workshop we will create an EC2 instance for our app layer and make all necessary software configurations so that the app can run. The app layer consists of a Node.js application that will run on port 4000. We will also configure our database with some data and tables.

Learning Objectives:
Create App Tier Instance
Configure Software Stack
Configure Database Schema
Test DB connectivity

ec2

In this section of the workshop we will create an Amazon Machine Image (AMI) of the app tier instance we just created, and use that to set up autoscaling with a load balancer in order to make this tier highly available.

Learning Objectives:
Create an AMI of our App Tier
Create a Launch Template
Configure Autoscaling
Deploy Internal Load Balancer

In this section we will deploy an EC2 instance for the web tier and make all necessary software configurations for the NGINX web server and React.js website.

Learning Objectives
Update NGINX Configuration Files
Create Web Tier Instance
Configure Software Stack


In this section of the workshop we will create an Amazon Machine Image (AMI) of the web tier instance we just created, and use that to set up autoscaling with an external facing load balancer in order to make this tier highly available.

Learning Objectives:
Create an AMI of our Web Tier
Create a Launch Template
Configure Auto Scaling
Deploy External Load Balancer










### Output Screenshots :

![Screenshot (228)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/03c6ace8-8444-4a3d-bf7f-25143bd52a31)

![Screenshot (230)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/d48cce72-c3f6-4f62-9a94-c6c3594b1b0b)
