---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Reimagining Security Engineering using Semgrep and OPA"
subtitle: ""
summary: "How tools like semgrep and OPA(Open Policy Agent) can trasform the way we do security engineering"
authors: [rohit]
tags: [threat_modelling,security]
categories: [Security]
date: 2024-04-16T15:00:03+05:30
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Security Engineering"
  focal_point: "smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects: []
---

In today's rapidly evolving technology landscape, ensuring the security of modern applications is a daunting task. With code running on containers in cloud environments, security engineers face the challenge of protecting not just the application itself but also its underlying infrastructure. Manual evaluation of security vulnerabilities is impractical given the volume and complexity of changes constantly being made. This is where tools like [Semgrep](https://semgrep.dev/) and [OPA (Open Policy Agent)](https://www.openpolicyagent.org/) come into play, providing the capability to identify and mitigate security risks proactively.

## Observing Changes

Security engineers are tasked with observing changes in four critical aspects of modern applications: code, containers, clusters, and cloud environments. Their responsibility is to ensure the confidentiality, integrity, and availability (CIA) triad is not compromised. While change is constant, security teams must not act as gatekeepers, which can slow down development processes. Instead, they should leverage automated tools like Semgrep and OPA to identify vulnerabilities as soon as they are introduced in the code.

## Utilizing Semgrep and OPA

Semgrep excels at identifying application bugs at the code level, while OPA focuses on policy violations across containers, clusters, and cloud environments. Semgrep can detect syntaxes of various languages and non-standard text to identify common vulnerabilities like injection, SSRF, XSS, and misconfigurations. On the other hand, OPA works seamlessly with JSON, allowing it to analyze Kubernetes manifest files, Terraform plans, and other JSON-formatted data to enforce security policies.

Identifying AWS Secret Keys with Semgrep:
- Semgrep rule detects AWS secret access keys leaked in source code.
  Example rule: https://semgrep.dev/playground/r/yeTQoe/generic.secrets.security.detected-aws-secret-access-key.detected-aws-secret-access-key 

Dockerfile Security Checks using OPA:
- OPA Rego policies enforce security baseline on Dockerfiles.
  Example implementation: https://medium.com/@madhuakula/dockerfile-security-checks-using-opa-rego-policies-with-conftest-32ab2316172f


## Building Custom Rules

Security engineers can develop custom rules for Semgrep and OPA based on threat models specific to their products. For instance, when building a user login page with Java backend and AngularJS frontend deployed as a Docker container on AWS EKS, threat cases can be translated into Semgrep and OPA rules

### Code

- Can someone perform an SSRF attack ? : Write a Semgrep rule to identify all possible places where java.net.URL or similar classes are being used and a tainted parameter is being passed to the class/function.
- Can an AWS Key be leaked ? : Write a semgrep rule that checks for AWS Key regular expression

### Container

- Is my container running as root ? : Write a Semgrep rule that checks for presence of a USER attribute in dockerfile or write an OPA rule that can check the same.
- Is my container building from an approved base image ? : Write a semgrep rule to check a regular expression that checks for the approved base image or write an OPA rule that can check the same.

### Cluster

- Are approved container images running in the cluster ? : Convert the K8s manifest file in JSON format and then check if images are compliant using OPA
- Are kubernetes deployments having memory and cpu utilizations ? : Convert the K8s manifest file in JSON format and then check if deployments have the memory and cpu utilisations defined using OPA.

### Cloud

- Are EC2 instances IMDSv2 compliant ? : Convert the terraform plan into JSON and then write OPA query to identify non-compliant IMDSv2 instances
- Are S3 Buckets with public access ? : Convert the terraform plan into JSON and then write OPA query to identify non-compliant S3 buckets

## Conclusion

By leveraging tools like Semgrep and OPA, security engineers can achieve a high level of security by continuously developing rules that align with specific threat models. Automation of security checks not only improves the security posture of modern applications but also enables faster development cycles. Embracing a proactive approach to security engineering empowers organizations to stay ahead of emerging threats in today's dynamic technological landscape

## Shameless Plug

My training titled “Securing Four Cs of a Software Product : AWS Edition '' exclusively focuses on tools like semgrep and OPA where students will understand how they can write semgrep and OPA rules and also integrate them into Github Actions. 

Checkout the Video Preview of my training here 

https://www.youtube.com/watch?v=HVU3nNbFJCo 

Registration Links for the training

3-4th August , Las Vegas , USA

https://www.blackhat.com/us-24/training/schedule/#securing-the-four-c39s-of-a-software-product-aws-edition-36609

5-6th August , Las Vegas , USA

https://www.blackhat.com/us-24/training/schedule/#securing-the-four-c39s-of-a-software-product-aws-edition-366091705526067 


[Image Credit: Freepik](https://www.freepik.com/free-vector/global-data-security-personal-data-security-cyber-data-security-online-concept-illustration-internet-security-information-privacy-protection_12953593.htm)
