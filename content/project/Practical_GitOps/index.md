---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Practical GitOps - Infrastructure Management using Terraform,AWS and Github Actions"
summary: "Practical GitOps is a book that will help you manage and automate your entire AWS infrastructure using Terraform and Github Actions"
authors: [rohit]
tags: [devops,gitops,docker,eks,route53,iac,aws secrets manager,opensearch,alb,terraform,terraform modules,prometheus,github,github actions,aws,aws iam,aws organisations,irsa,kubernetes]
categories: [Technology]
date: 2022-12-30T16:04:59+05:30
toc: true

# Optional external URL for project (replaces project detail page).
# external_link: "https://github.com/salecharohit/devops"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
# image:
#   caption: "Practical DevOps Lab"
#   focal_point: "Smart"
#   preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: "https://link.springer.com/book/10.1007/978-1-4842-8673-9"
url_pdf: "https://www.amazon.com/Practical-GitOps-Infrastructure-Management-Terraform/dp/1484286723"
url_slides: ""
url_video: ""
asciinema : false
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
## Motivation

In 2018, I heard the term **Kubernetes** for the first time, and the only understanding I had of AWS was that we can run machines in the cloud that can be accessed from anywhere. Being in the security domain, hearing new technology terms and learning about these technologies has been an undying passion of mine. It took me two years to understand DevOps, and I created a small
hobby project called [Practical DevOps lab]({{< relref "project/Practical_DevOps/index.md" >}})
 to help people understand the core
underlying technologies that make up the umbrella term.

After completing this, I asked myself what’s next?

So I decided to level up and started to explore cloud and cloud-native technologies like AWS and Kubernetes and how they can be set up using Infrastructure as Code like Terraform and hence this book. I wouldn’t say that I am an expert at any of these technologies
because that was never my aim. My aim was to have a basic hands-on understanding of them, and in this book, I am sharing that limited
knowledge that I have because being from the security domain, it’s my job to help organizations secure their assets, but if I don’t have a basic understanding of what they are, then I wouldn’t be doing my job well.

## About The Book

Infrastructure as Code (IaC) is gaining popularity and developers today are deploying their application environments through IaC tools to the cloud. However, it can become extremely difficult and time-consuming to manage the state of the infrastructure that has been deployed. This book will provide a complete walkthrough of deploying a SpringBoot application on AWS with multiple environments like production, staging and development. Everything is orchestrated through GitHub Actions and executed through Terraform Cloud to monitor changes in your infrastructure and manage its state. 

You'll start by reviewing how your infrastructure can be stored in code by spinning up an EC2 server first through the console, then AWS CLI and then using Terraform. You'll then be presented with a practical scenario of setting up a simple EC2 server in a multi-environment (production, staging and development) using GitHub Actions and Terraform Cloud. In the advanced section that follows, this simple EC2 server is expanded into an application that is deployed on an AWS EKS (Elastic Kubernetes Service) using AWS RDS (Relational Database Service) exposed through an AWS ALB (Application Load Balancer) protected using AWS ACM (AWS Certificate Manager), and accessible by setting the AWS Route53. 

The book then builds up on this infrastructure and demonstrates how it can be deployed in a multi-environment scenario by implementing accounts through AWS organizations. You'll see how to put in restrictions through Service Control Policies, how to protect secrets using AWS Secrets Manager, and how to work with least privileges using IRSA (IAM Roles for Service Accounts). Finally, you'll make the infrastructure more observable using Graphana, Prometheus, and AWS OpenSearch, run security tools, host Route53 zones dynamically based on environments, and implement CloudWatch Alarms for various use cases.

## What to expect ?

- Learn how you can deploy a multi-stage/multi-environment cloud and cloud native infrastructure using Terraform and Github Actions
- AWS Services that you can deploy/operate/manage using Terraform in this book
    - AWS EKS
    - AWS RDS
    - AWS ALB
    - AWS Organisations and Creating Multiple Accounts tied with environments
    - AWS IAM(Users,Groups,Roles and Permissions) and SCPs
    - IRSA using IAM OIDC
    - AWS OpenSearch
    - AWS Secrets Manager
    - AWS KMS
    - AWS CloudTrail
    - AWS CloudWatch Alarm
    - AWS SNS
    - AWS Route53
    - AWS ACM
- Other than AWS below are the other open source tools/technologies used everything using Terraform and Github Actions
    - Karpenter Auto-Scaler
    - Checkov
    - Secrets Store CSI Driver
    - Prometheus
    - Graphana
    - Kubernetes RBAC tied to AWS IAM
    - Terraform Cloud

## Where to buy ?

If you want raw PDF you can buy it directly from Springer using the link below

https://link.springer.com/book/10.1007/978-1-4842-8673-9 

If you are a kindle fan , buy it from Amazon

https://www.amazon.com/Practical-GitOps-Infrastructure-Management-Terraform/dp/1484286723

## Complete ToC

### Chapter 1: What Is GitOps?
- 1.1 The Era of DevOps
    - 1.1.1 What Problems Is DevOps Addressing?
- 1.2 Introduction to DevOps
    - 1.2.1 Continuous Integration
    - 1.2.2 Continuous Delivery/Deployment
    - 1.2.3 Continuous Monitoring
- 1.3 Infrastructure As Code (IaC)
    - 1.3.1 Evolution of Server Infrastructure
    - 1.3.2 Tools of Trade – IaC
    - 1.3.3 Mutable vs. Immutable Infrastructure
    - 1.3.4 State in IaC
- 1.4 Problems with Continuous Delivery
- 1.5 Introduction to GitOps
- 1.6 Conclusion

### Chapter 2: Introduction to AWS
- 2.1 Prerequisites
- 2.2 Introduction to AWS
    - 2.2.1 Create an AWS Account
    - 2.2.2 Log in into the AWS Account
- 2.3 Creating an EC2 Machine – GUI
    - 2.3.1 Default Region Selection
    - 2.3.2 Instance Type Selection
    - 2.3.3 Instance Configuration
    - 2.3.4 Instance Storage
    - 2.3.5 Tags
    - 2.3.6 Security Groups
    - 2.3.7 SSH Key-Pair Generation
    - 2.3.8 Launching EC2 Instance
    - 2.3.9 Terminating EC2 Instance
- 2.4 Creating an EC2 Machine – CLI
    - 2.4.1 Configuring CLI Environment
    - 2.4.2 Fetching Security Group ID
    - 2.4.3 Fetching Subnet ID
    - 2.4.4 Launching EC2 Instance
    - 2.4.5 Accessing EC2 Instance
    - 2.4.6 Terminating EC2 Instance
- 2.5 Clean-Up
- 2.6 Conclusion

### Chapter 3: Introduction to Terraform
- 3.1 Prerequisites
- 3.2 Introduction to Terraform
- 3.3 Getting Started with Terraform
- 3.4 Iteration #1
    - 3.4.1 Terraform Working Directory
    - 3.4.2 Terraform init
    - 3.4.3 Terraform Plan
    - 3.4.4 Terraform Apply
    - 3.4.5 Terraform State File
    - 3.4.6 Terraform Destroy
- 3.5 Iteration #2
    - 3.5.1 Terraform Variables
    - 3.5.2 Terraform Data Source
    - 3.5.3 Terraform Resource
    - 3.5.4 Terraform Output
- 3.6 Iteration #3
    - 3.6.1 Terraform Modules
- 3.7 Selective Destroy
    - 3.7.1 Terraform Destroy Protection
- 3.8 Terraform Drift
- 3.9 Clean-Up
- 3.10 Terraform Commands Reference
- 3.11 Conclusion

### Chapter 4: Introduction to Terraform Cloud
- 4.1 Prerequisites
- 4.2 Terraform State Management
- 4.3 Introduction to Terraform Cloud
- 4.4 Terraform Cloud – Getting Started
    - 4.4.1 Creating a Workspace
    - 4.4.2 Configure Workspace
    - 4.4.3 Workspace Variables
    - 4.4.4 Terraform Login
    - 4.4.5 Running Terraform in Terraform Cloud
    - 4.4.6 Terraform Cloud Run and States
- 4.5 Multi-environment with DRY
    - 4.5.1 Adding Production Environment
    - 4.5.2 TF Variables Overriding
- 4.6 Clean-Up
    - 4.6.1 Destroying Terraform Cloud Workspaces
- 4.7 Terraform Cloud Security Best Practices
- 4.8 Conclusion

### Chapter 5: Terraform Automation with Git
- 5.1 Prerequisites
- 5.2 Terraform Automation with GitHub
    - 5.2.1 Setting Up the GitHub Repository
    - 5.2.2 Connecting GitHub with Terraform Cloud
    - 5.2.3 Creating VCS-Driven Workspace
    - 5.2.4 Configuring Environment Variables
    - 5.2.5 Executing Plan in Cloud
    - 5.2.6 Triggering the VCS
    - 5.2.7 Destroying in Terraform Cloud
    - 5.2.8 Drawbacks of Terraform Cloud with VCS
- 5.3 Introduction to GitHub Actions
    - 5.3.1 CI/CD General Workflow
    - 5.3.2 Introduction to GitHub Actions
    - 5.3.3 Sample GitHub Actions YAML
    - 5.3.4 Docker Build Automation with GitHub Actions
    - 5.3.5 Triggering GitHub Actions
- 5.4 Terraform Automation with GitHub Actions
    - 5.4.1 Code Walkthrough
    - 5.4.2 Terraform Login Token
    - 5.4.3 Creating an API-Driven Terraform Workspace
    - 5.4.4 Executing API-Driven Workflow
- 5.5 Clean-Up
- 5.6 Conclusion

### Chapter 6: Practical GitOps
- 6.1 Prerequisites
- 6.2 Staging Environment Workflow
    - 6.2.1 High-Level Plan
    - 6.2.2 Code Walkthrough
    - 6.2.3 Set Up Terraform Staging Workspace
    - 6.2.4 Set Up a GitHub Repository
    - 6.2.5 Executing Staging Workflow
- 6.3 Prod Environment Workflow
    - 6.3.1 SSH Key-Pair Generation
- 6.4 Complete Workflow
    - 6.4.1 New Feature Request
    - 6.4.2 Developer Testing
    - 6.4.3 Create Pull Request – Dev
    - 6.4.4 Create Pull Request – Prod
- 6.5 Clean-Up
- 6.6 Conclusion

### Chapter 7: Spring Boot App on AWS EKS
- 7.1 Prerequisites
    - 7.1.1 GitHub Repository
    - 7.1.2 DNS Configuration
- 7.2 Solution Architecture
- 7.3 Networking
    - 7.3.1 Network Module
    - 7.3.2 Network Tags
    - 7.3.3 Security Groups
- 7.4 Database
    - 7.4.1 Database Module
    - 7.4.2 Database Configuration and Secrets
- 7.5 Kubernetes
    - 7.5.1 EKS
    - 7.5.2 EKS Module
    - 7.5.3 EKS Worker Nodes
    - 7.5.4 EKS Security Groups
    - 7.5.5 EKS Ingress Controller
- 7.6 DNS
    - 7.6.1 Route53 Record Creation
    - 7.6.2 Multi-environment DNS
    - 7.6.3 ACM
- 7.7 Application
    - 7.7.1 Namespace
    - 7.7.2 Deployment
    - 7.7.3 NodePort Service
    - 7.7.4 Ingress
    - 7.7.5 Kubernetes Provider
    - 7.7.6 Variables
    - 7.7.7 Default Environment
- 7.8 Execution
    - 7.8.1 Setting Up the EKS Cluster
    - 7.8.2 Accessing the EKS Cluster
- 7.9 Clean-Up
- 7.10 Conclusion

### Chapter 8: Authentication and Authorization
- 8.1 Prerequisites
    - 8.1.1 Code Update
- 8.2 AWS Organizations
    - 8.2.1 Root Account
    - 8.2.2 Member Accounts and OUs
    - 8.2.3 AWS Provider
- 8.3 AWS IAM
    - 8.3.1 IAM Users
    - 8.3.2 IAM Groups
    - 8.3.3 IAM Roles
- 8.4 AWS Route53
- 8.5 Executing Global
    - 8.5.1 Generate GNU PG Keys
    - 8.5.2 Configure Variables
    - 8.5.3 Terraform Cloud Workspace
    - 8.5.4 Terraform Apply
    - 8.5.5 Terraform Output
    - 8.5.6 Possible Issues
- 8.6 EKS Authz
    - 8.6.1 EKS Client Authentication
    - 8.6.2 EKS Node Authentication
    - 8.6.3 Provider Configuration
- 8.7 Executing Infra
    - 8.7.1 AWS Profiles
    - 8.7.2 Development
    - 8.7.3 Staging
    - 8.7.4 Prod
- 8.8 EKS Access Control
- 8.9 Clean-Up
    - 8.9.1 Dev
    - 8.9.2 Staging/Prod
- 8.10 Conclusion

### Chapter 9: Security and Secrets Management
- 9.1 Code Update
    - 9.1.1 Committing only Global
    - 9.1.2 Committing Infra
- 9.2 Enhancing EKS Security
    - 9.2.1 Encrypting K8s Secrets
    - 9.2.2 Encrypting EKS EBS
    - 9.2.3 Enhancing EC2 Metadata Security
- 9.3 Enhancing AWS ALB Security
- 9.4 Restricting RDS Exposure
- 9.5 Secrets Exposure
    - 9.5.1 Terraform State
    - 9.5.2 Kubernetes Deployment Descriptions
- 9.6 AWS Secrets Manager
    - 9.6.1 Secrets Management Design
    - 9.6.2 Secrets Store CSI Driver
- 9.7 IRSA
    - 9.7.1 Background
    - 9.7.2 Internal Working
    - 9.7.3 IAM Permissions Policy
- 9.8 Checkov Scanning
    - 9.8.1 Checkov in Action
- 9.9 Service Control Policies
    - 9.9.1 SCP in Action
- 9.10 Clean-Up
- 9.11 Conclusion

### Chapter 10: Observability
- 10.1 Code Update
    - 10.1.1 Committing Only Global
    - 10.1.2 Committing Infra
- 10.2 Executing Infra
- 10.3 Organization Trail
- 10.4 CloudWatch Alarm
    - 10.4.1 Configuring AWS SNS
    - 10.4.2 Configuring CloudWatch Alarm
    - 10.4.3 Root Login Alarm in Action
- 10.5 Master Account Login
- 10.6 ALB Access Logs
- 10.7 Logging
    - 10.7.1 Exploring OpenSearch
- 10.8 Monitoring
    - 10.8.1 Exploring Grafana
- 10.9 Karpenter Autoscaler
    - 10.9.1 Karpenter in Action
- 10.10 Upgrading Kubernetes
- 10.11 Clean-Up
- 10.12 Conclusion

- Annexure A: Manually Delete Resources
- Annexure B: Terraform Cloud Destroy Problem
- Annexure C: Code Compatibility on OS