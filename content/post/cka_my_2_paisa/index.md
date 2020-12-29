---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "CKA My 2 Paisa"
subtitle: ""
summary: "My experience of completing the Certified Kubernetes Administrator(CKA) course"
authors: [rohit]
tags: [CKA]
categories: [Technology]
date: 2020-12-29
lastmod: 
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Certified Kubernetes Administrator"
  focal_point: "Center"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: [Practical_DevOps]
---

Today on 29th December I passed my CKA(Certified Kubernetes Administrator) course !

I'd like to share my experience and some tips,tricks and notes for attempting this certification through this post.

Before you begin you need to to first ask yourself, why you need to do this certification?

# Motivation

I wanted to learn Kubernetes primarily from two perspectives
- I have been learning about DevOps and allied technologies and what I realised is that Container Orchestration is one of the most central component in the CI/CD framework and Kubernetes is most popular in this domain. Hence, I wanted to learn Kubernetes to enhance my [DevOps Lab project]({{< relref "project/Practical_DevOps/index.md" >}}) which I shall now start working on soon to integrate Kubernetes.
- With high adoption for Kubernetes I wanted to get a perspective on Kubernetes security for which the CKS(Certified Kubernetes Security) certification has been designed. However in order to attempt CKS i first need to pass CKA.

# Preparation

- So i started off with [Kubernetes for the Absolute Beginner](https://kodekloud.com/p/kubernetes-for-the-absolute-beginners-hands-on) and then moved ahead with [CKA with practice tests](https://kodekloud.com/p/certified-kubernetes-administrator-with-practice-tests) which I absolutely recommend especially for their labs infrastructure.
- Another good resouce you can look for is [https://kubernetesbyexample.com/](https://kubernetesbyexample.com/) which you can use in conjuction with the labs provided by KodeKloud.
- Once I would finish a topic in the KodeKloud labs I also spent time reading the corresponding documentation located at [https://kubernetes.io/docs/concepts/](https://kubernetes.io/docs/concepts/). This was very necessary for me because it helped in regurgigating what I've learnt.
- After having completed the entire labs provided by KodeKloud 2 times, I skimmed through all the tasks provided in the documentation located here[https://kubernetes.io/docs/tasks/](https://kubernetes.io/docs/tasks/). I *very strongly recommend* that you go through these tasks atleast twice before attempting the exam.
- While studying for Kubernetes the only topic I found extremely tricky to understand was Network Policies and this is by far the best read on NetPols [https://github.com/ahmetb/kubernetes-network-policy-recipes](https://github.com/ahmetb/kubernetes-network-policy-recipes)
- I signed up for [killer.sh](killer.sh) as well for additional practice, definitely recommended because in KodeKloud's infrastructure you are directly logging into the controlplane or master node. Whereas in killer.sh they mimic the exam by giving you a shell on the edge node rather than directly on the master node which did help me.
- The exam signup process was quite straight forward and many people have written about it however few tips I can share for the exam
  - I gave the exam in a dual monitor mode by duplicating the screens. This was really helpful for me because I can view the screen on a bigger surface.
  - Create a new profile in Chrome/Chromium especially for the exam and bookmark the documentation and the tasks pages.

For CKA preparation I can speak of only two words, Practice and Documentation. Practice can be done through KodeKloud and Killer.sh but It needs to be backed-up by atleast reading the kubernetes.io documentation. Knowing the documentation will also help navigating through it quickly during the exam.

I hope you find my notes useful and I wish all the very best for your attempt !

> Please note that I won't be soliciting any questions regarding what was asked in the exam owing to the non-disclosure agreement.