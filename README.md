# AWS 3 Tier Web Architecture

Hosting a 3 tier Web App in AWS 

### this is the architecture of the project

![3TierArch](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/fd09b3f6-f07f-487c-ba5d-2f9a038a7ef8)

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.
### writing an terraform HCL and hosting an simple website 


![Screenshot (223)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/126942ce-60fd-496c-a6d3-0fcfca55dc84)


rds
![Screenshot (224)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/895f1519-f0e2-453c-9e0f-7eb4f71d521b)


installing mysql
![Screenshot (226)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/99dd8dfa-4ee3-4a71-9472-556d62c64486)

s3 bucket
![Screenshot (227)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/2618b914-b758-4aed-ad12-d0157e64f75a)

ec2






output
![Screenshot (228)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/03c6ace8-8444-4a3d-bf7f-25143bd52a31)

![Screenshot (230)](https://github.com/sunilkurthakoti/AWS_3tier_web_architecture/assets/131526336/d48cce72-c3f6-4f62-9a94-c6c3594b1b0b)
