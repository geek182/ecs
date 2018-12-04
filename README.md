# ecs
using ecs

ECS Cluster
ec2
fargate

Task definition
TaskSize ( cpu and memory limits )
Container Level
Docker image
* cpu and memory limits
* Port mapping (0 for random on host)
* Health Checks
* Volumes
* LogConfiguration
* TaskSize ( cpu and memory limits )

Service
Service Type
Desire State
LoadBalance
Task Definition

steps:

#Start a service
ecs-cli compose --cluster cluster-name -f docker-compose.yml --ecs-params ecs-params service up

#Stop a service
ecs-cli compose --cluster cluster-name -f docker-compose.yml --ecs-params ecs-params service down

#Tag
docker tag web-nginx:latest ecr-url/web-nginx:tag

#push to ECR
ecs-cli push ecr-url/web-nginx:tag
