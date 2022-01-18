# DeployMicroservices-AWS-ECS
Cloud formation script to create AWS services - IAM role, Parameter store, Secret manager, Load Balancer, Target groups ECS Task definition, ECS services with Autoscaling policy and ECS Fargate cluster

**Prerequisite**

1. AWS environment
2. Create 3 ECR repository and push docker images - (1 for UI and remaining 2 microservices are backend)

**Run Cloudformation template**
This cloudformation template will create 3 serverless microservices in ECS containers. 
Ideally I have used 1 microservice for Angular front end application, 2 microservices for backend API (developed in .net core). 
2 backend microservices are Dashboard and Admin service. Admin service accessed by users with specific role and Dashboard service accessed by loggedin user. 
So 2 microservices has been developed for backend.

Authentication has been implemented in Angular SSO using Azure.
Authorization has been implemented using Azure AD Identity server

Run the ECS-Microservices.yml in AWS cloudformation by providing proper parameters. This template will create following AWS resources

1. IAM Roles
2. ECS Task definition
3. Container Security Group
4. LoadBalancer Security Group
5. Application Load Balancer
6. Load Balancer Http Listener
7. Target group
8. ECS Fargate cluster
9. ECS container services
10. ECS Task definition
11. Auto scaling policy
12. Log group in cloudwatch
