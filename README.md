# 3.11-ECS-Fargate

1. Create ECS cluster with Fargate to deploy NGINX web application into AWS using Terraform Code and Github Actions.
2. Terraform Code will perform creation of below resources.
3. Create ECS Cluster
4. Create Task Definition, this is a json file contain all configuration.
5. Create ECS Service to deploy task definition with an application load balancer
6. Final, view the NGINX web application using public ip address and DNS name.
7. Github Actions worksflow : ecs_create.yml
8. This worksflow will perform following tasks when git push is trigger.
  - Terraform create - Apply all terraform code to create ecs cluster, ecs task definition, ecs service and application load balancer.
  - Terraform wait - A waiting times of 4 minutes to check the ecs status in AWS and view the NGINX web application using IP address or DNS name.
  - Terraform destroy - This will do the clean up process where all the resources created will destroy.
