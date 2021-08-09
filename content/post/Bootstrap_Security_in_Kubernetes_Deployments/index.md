---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Bootstrap Security in Kubernetes Deployments"
subtitle: "Learn how to practically boostrap security controls into your kubernetes deployments"
summary: "Learn how to practically boostrap security controls into your kubernetes deployments"
authors: [rohit]
tags: [devops,kubernetes,security]
categories: [Security]
date: 2020-08-07T15:46:03+05:30
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Kubernetes Security"
  focal_point: "smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects: []
---

Kubernetes, is one of the [most popular and most used](https://devopscube.com/docker-container-clustering-tools/) container orchestration tool. [Kubernetes Workloads](https://kubernetes.io/docs/concepts/workloads/) are the actual applications that are executed like a simple nginx server or maybe a cron job. [Kubernetes Deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) is the [most commonly used](https://rancher.com/learning-paths/introduction-to-kubernetes-workloads/#:~:text=Deployments%20are%20one%20of%20the,updates%2C%20rollbacks%2C%20and%20scaling.) workload as it can be easily updated,scaled and managed.

The recently released [Kubernetes Hardening Guide](https://media.defense.gov/2021/Aug/03/2002820425/-1/-1/1/CTR_KUBERNETES%20HARDENING%20GUIDANCE.PDF) is an excellent resource that provides a proper guidance on how to effectively secure Kubernetes. The information presented in the guide clearly shows that securing and hardening kubernetes is not just the job of the Kubernetes administrator but also of the developers who are deploying their workload on the clusters. The guide mentions about Pod Security and namespace segregation which is something the developers and architects need to be concerned about.

In this blog I'll discuss about how developers deploying Kubernetes workloads like Deployments can bootstrap security by applying implementing some of the guidelines provided by the Kubrnetes Hardening guide.

This will be a practical hands-on guide where I shall take a simple Dockerfile and then incrementally add the security best practices to **create a template Deployment manifest file** which can then be reused by developers in a hurry.

## Pre-Requisites

- Docker is required as we'll be building from ground up.
- A single-node Kubernetes cluster like minikube should be sufficient to follow along with this guide alongwith the kubectl utility. You can use the [official minikube](https://minikube.sigs.k8s.io/docs/start/) documentation.

I am using a standalone cluster created by [Docker Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows) tied to WSL2 as the backend.

![Docker Desktop](img/1.png) 

This guide from henceforth will assume that you have a running cluster to which is accessible through the kubectl utility as shown above.

## Securing Deployments

Securing the kubernetes workloads can effectively be compartimentalised into 'Buildtime' and 'Runtime' security.

### Build Time Security

Buildtime security focusses more on how the underlying containers can be build with a reduced footprint and are programmed to be executed with least possible privileges. 

For Ex: if we need to run a simple nginx server to host some HTML files we practically donot need the baggage of libraries like glibc which are pre-baked into the default docker images.

#### Attack Surface Reduction

#### Switching User Context

### Runtime Security

#### Immutable File-Systems

#### Service Account Tokens

#### Pod Security Contexts



