# AWS 3 Tier Web Architecture

## Overview:
In the AWS 3 Tier Web Architecture, we deploy a robust and scalable web application utilizing Amazon Web Services. The architecture comprises three tiers: web, application, and database. The application load balancer manages traffic, routing it through EC2 instances in the web tier, then to the application tier, and finally interacting with an Aurora MySQL multi-AZ database.

### 1. Architecture Overview:
![3-Tier Architecture](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/fd09b3f6-f07f-487c-ba5d-2f9a038a7ef8)

This diagram illustrates the flow of client traffic through an Application Load Balancer to Nginx webservers in the web tier, Node.js application servers in the application tier, and finally, to an Aurora MySQL database. Load balancing, health checks, and autoscaling groups are implemented at each layer for enhanced availability.

### 2. VPC and Networking Configuration:
![VPC and Networking](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/126942ce-60fd-496c-a6d3-0fcfca55dc84)

The VPC and networking components are configured to establish a secure and isolated network. This includes the creation of a VPC, subnets, route tables, internet gateway, NAT gateway, and security groups for EC2 instances, Aurora databases, and Elastic Load Balancers.

### 3. S3 Bucket Setup and File Upload:
![S3 Bucket](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/2618b914-b758-4aed-ad12-d0157e64f75a)

An S3 bucket is created to store and manage static files. The architecture involves uploading essential files to this bucket for use in the web application.

### 4. RDS Configuration:
![RDS Configuration](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/895f1519-f0e2-453c-9e0f-7eb4f71d521b)

The database layer is configured using Aurora MySQL. This section involves creating an EC2 instance for the app layer, configuring the software stack, and setting up the database schema.

### 5. Autoscaling and Load Balancing (App Tier):
In this phase, an Amazon Machine Image (AMI) is created for the app tier instance, enabling autoscaling and load balancing. This ensures high availability of the application.

### 6. Web Tier Configuration:
An EC2 instance for the web tier is deployed, involving necessary software configurations for NGINX web server and React.js website.

### 7. Autoscaling and Load Balancing (Web Tier):
Similar to the app tier, an AMI of the web tier instance is created to establish autoscaling and load balancing for high availability.

### 8. Output Screenshots:
![Output Screenshot 1](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/03c6ace8-8444-4a3d-bf7f-25143bd52a31)

![Output Screenshot 2](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/d48cce72-c3f6-4f62-9a94-c6c3594b1b0b)

This architecture demonstrates a comprehensive and scalable approach to hosting a 3-tier web application on AWS, ensuring high availability, efficient load balancing, and secure networking configurations.
