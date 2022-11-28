# join-devops-challenge

## Task details
https://github.com/join-com/devops-challenge#instructions

## Core Objectives
- Created the necessary kubernetes files using helm which creates 2 instances of each microservice
- The helm charts can be executed in any cluster by running the script "helm/helm_install.sh" to bring up all the objects. I had tested it within a minikube cluster in ec2 instance. 
- Only /calc of acceleration-calc microservices is made available using ingress
- Ensured stability of application by adding liveness probe. When the api requests timeout after the configured period, pods would restart automatically. 
- Used multi-stage docker build to keep the production containers light. 

## Enhancements
- Planning for enhancements as I find more time

## CICD
- Configured basic CICD using azure devops which is triggered on any change within the repo. Link - https://dev.azure.com/sabm/sabm/_build?definitionId=2 
- Consists of two stages - 1.Rebuild the docker image and pushes it to registry with latest changes  2.Perform helm upgrade to deploy the change
- Ideally, there should be more stages such as unit test, static code analysis, SCA/SAST scans, etc
