---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Shift Left, Scale Up Security Using Threat Modelling"
subtitle: "How to shift left and scale up your security using threat modelling"
summary: "Security today not only needs to be shifted more towards the developers but also needs to be scaled up to reduce the dependency on the security teams. Let's see how that is possible using Threat Modelling"
authors: [rohit]
tags: [threat_modelling,security]
categories: [Security]
date: 2021-09-15T15:46:03+05:30
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Threat Modelling"
  focal_point: "smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects: []
---

Security strategies today for most organisations is to 
- Shift Security left more towards the developers
- Engage developers/architects in security processes so as to scale up

Both these points are mutually inclusive i.e. need to be done hand-in-hand. One cannot scaleup security without shifting more towards the left and vice versa. If focus is trained on any one of them then the organisation will end-up in a catch-22 situation.

## Addressing the Catch-22

The answer is simple ,**Threat Modelling** , which is now even recommended in the new [OWASP Top 10 - 2021](https://owasp.org/Top10/) in the form of `A04:2021-Insecure Design`. 

> Currently the new Top 10 is still in the DRAFT stage however, the comunity identifying this as a weakness certainly calls for a change in the way manage security across our organisations.

## What is Threat Modelling ?

There are many definitions out there describing threat modelling but in extremely simple terms it is an attempt to identify threats even before the application/feature development starts. Some example threats
- A Potential security flaw being exploited
- Data leakage
- Business continuity being affected
- Privilege Escalation
- Customer confidence going down and many more ...

One of the best resources that I found is [Segment's Threat Modelling Training](https://github.com/segmentio/threat-modeling-training) that they developed internally with an intent to scale up security.

## Issues with Adoption of TM

Not many organisations are able to adopt Threat Modelling as a process because

- Most of the times Architecture diagrams and other application artefacts like documentation,functional and non-functional requirements are not updated or not captured. Hence contextual information is absent.
- In absence of a proper context its difficult to derive threat models
- Developers/technical architects are quite averse to using security tools.
- Generally a threat modelling tool would spool out quite a lot of threats which overhwhelms the developers leading to friction.

## How To ScaleUp + ShiftLeft ?

So how exactly can we scale up and shift left security using Threat Modelling ?

Let's analyse that through the lens of People,Process and Technology, the three pillars of success for any organisation.

### People

We'll need two sets of profiles here that are mostly in a mid-senior roles who are an expert in their domain

- Technical Architect
  - Should have hands-on experience with software development best practices.
  - Should be able conceptualise and visualise the architecture of a particular application/product/service alongwith its integrations.
  - Should be responsible and accountable for creation and maintenance of the relevant artefacts of a particular application like Architecture Diagrams,Data Flow Diagrams,UMLs,Functional and non-functional requirements,source code etc ...
  
  This is just a very brief of the roles and responsibility of a Technical Architect. Below are some guides for a much more detailed job description
  - [What Does a Technical Architect do - Randstad](https://www.randstad.co.uk/career-advice/job-profiles/what-does-a-technical-architect-do/)
  - [Technical Architect Job Description - Workable](https://resources.workable.com/technical-architect-job-description)

- Security Architect
  - Should be able to enumerate the threats by understanding the application's assets created by the Technical Architects.
  - Should have a broad understanding of technology components so as to evaluate the risks associated with it. For Ex: most organisations today are migrating to Kubernetes,hence a Security Architect must have some knowledge of how Kubernetes works and how is it being operated not necessary a hands-on,deep dive knowledge.
  - Provide countermeasures for the identified threats through a medium and context that developers understand.
  - [Security Architect: Job role at a glance - Aarushi Koolwal](https://aarushikoolwal.com/post/security-architect-job-role-at-a-glance/) is a fantastic article describing more about the Security Architect job role.

### Technology

In order for the Technical Architect(TA) and Security Architect(SA) to scale up their work they'll need tools.
A tool that can cater to both their requirements.

- The interface of the tool should be developer friendly so that she can create architecture diagrams and input application requirements with ease.
- Once the requisite information from the TA is received the tool should be able to evaluate the information and generate threats and countermeasures.
- Tool must also integrate with whatever ticketting system is being used by the developers to track issues. 
- The sync between the tool and the ticketting system should also be bi-directional as this will help security architects track issues that've been closed.

### Process

- The Technical Architect should prepare the relevant application artefacts like app documentation,relevant diagrams , requirements etc ... and add them in the threat modelling tool.
- She should be able to present the artefacts to all relevant stakeholders for any new feature/change or a new project altogether by keeping this tool as the point of reference.
- Security architects would review the artefacts and the diagrams in the threat modelling tool, remove false +ves and other noise and then add the threats with their countermeasures as a requirement/user story.
- Developers can now work on the security requirements alongside other features.

## How Would this Help?

- With this technique Technical Architects would keep their Architecture Diagrams and other artefacts "Live" and continue to update in the same tool. Hence TA's are now using this tool for their own purpose and not necessarily for security.
- Security Architects can keep track of changes and accordingly provide their security requirements by filtering out the noise.

> Basically both teams are now working on the same platform and performing their own jobs while at the sametime collaborating with each other ! Hence, we are solving two problems with a single solution.






