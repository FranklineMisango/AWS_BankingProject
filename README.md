# Project Description

## Business Objective
MLOps is a means of continuous delivery and deployment of a machine learning model.  Practicing MLOps means that you advocate for automation and monitoring at all steps of ML system construction, including integration, testing, releasing, deployment, and infrastructure management. In this Task, you will be deploying the machine learning application for the Build Classification Algorithms for Digital Transformation [Banking].We have generated the .sav file. This project uses Amazon EKS (cloud platform), Amazon EC2, Elastic Load Balancing, etc services. Amazon EKS is a fully managed service that makes it easy to deploy, manage, and scale containerized applications using Kubernetes on AWS.

 ## Aim
Deploy a machine learning model to identify the potential borrower customers to support focused marketing and deploy them through a cloud provider (AWS)
## Tech stack
    Language - Python
    Services - AWS EKS, ECR, Load balancer, code commit, code deploy, code pipeline
## Prerequisites
It is advisable to have a basic knowledge of the following services to get an understanding of the project.
    Flask
    Aws ECR
    AWS ECS
    AWS EC2 Load balancer
    AWS Code commit
    AWS Code Build
    AWS Code Deploy
    AWS Code Pipeline
## Approach
* Cluster creation steps
        Create an EKS cluster master node.
        Create Node groups in the EKS cluster
        Create OIDC connection in the AWS Identity provider with EKS cluster
        Install Kubernetes dashboard for monitoring
        Install AWS Load balancer controller
* Create an ECR repository for the docker image
* EKS Yamls for our application
        Create deployment yaml
        create service yaml
        create ingress yaml
* Code Pipeline for EKS
        Create 2 code commit repositories one for flask ml application and another one for EKS yamls
        Create 2 code build projects one for flask ml application and another one for EKS yamls
        Create 2 code pipelines one for flask ml application and another one for EKS yamls
* In the EKS yaml code pipeline, have both ECR repo and code commit repo as the source
* Push ML application into EKS
        Create Flask application for our ML Application
        Convert that Flask application into a docker Application
        Test the docker application in your local
        Push the Flask code to code commit, check the pipeline runs without any issues.
        Once the Flask code pipeline ran successfully, check whether it triggers the second EKS yaml code pipeline.
        If the second pipeline is triggered, check the API response for the update values.

