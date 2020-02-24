---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Demystifying Agile Scrum"
subtitle: "Understand the keywords of Agile and Scrum"
summary: "Understand the keywords of Agile and Scrum in perspective of software development"
authors: [rohit]
tags: [agile,scrum]
categories: [Technology]
date: 2019-03-04T22:28:30+05:30
lastmod: 2019-12-05T22:28:30+05:30
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

For one of a project, i was required to learn and trained on Agile-Scrum framework for Software development. Being a security professional, it wasn't much of use for me but i really wanted to know what exactly is this new framework all about so that everyone on the team is on the same page. More importantly, I wanted to understand how is it different from the traditional SDLC process of software development.

The following pictures, is a TL;DR of the difference between the SDLC process and the Agile Process

#### Typical SDLC Process

![Typical SDLC Process](https://lh6.googleusercontent.com/B66soHV9_N0R5EfMltKoOerTi3vTvt3z0a7Cetk-coGHeFi0U70i3O4TL5jI1LMz9BKAW6ZNzJWYQct59P4oDKWqHDJwaPOTLe-RcBVZgkGWGi_WChhw1CudiLi69_VHDPpsevb4)

#### Agile Process

![Agile Process](https://lh3.googleusercontent.com/Zwo8ktco7IKgjpn0GZeTC32DDJADcX_Eef3OjmntqPgel9CyZyb8G-Rjwmq6vi3lM-1BBiof2J5bnFnGtnKNRKUdZqY4AcynLRUBr7nqZozq1tgDpkRiuQr_JDjG21TlFVQcGSHa)

Lets say we want to develop a Shopping Cart application over a period of 6 Months. In a typical SDLC process , we would first sit with the client and gather all their requirements. This requirements gathering stage would take approx 1 Month. After this , we would go to our design studio , and create a high level design of the application which would take another 15 days.During this time, we would also assemble the team and start the development which would take a yet another 3-4 Months. Once we do a UAT test of the application, we invite the client (after 6 months) and show them the product.

The client gives some feedback and is usually not happy with the product. Then starts the roller coaster ride wherein everyone is already burnt out and performance goes down.

Now, lets apply some common sense, and say, that we take the following requirements and develop it quickly in about 3 weeks.

1. Ability to view the product details including the images
2. Search function for searching various products
3. A large menu item which would display most categories of the product
4. A shopping cart where customers can put their selected items

We complete this much and show it to the client. The client now gives some feedback saying that he also wants recently viewed items. We take that into consideration and start a yet another dev cycle including the following requirements.

1. Customers should be able to login to create their own profile including their address and contact details
2. Ability to make different types of payments for the products selected in the shopping cart.
3. Ability to view recently viewed items.

Now, in addition to the first 4 requirements, after 3 weeks we show the customer the above functionality and is really happy to see the new website live in production. At this stage , the customer also feels that we should deploy the site into production with the limited features that we have now developed.

Now, if you compare this with the typical Waterfall SDLC process , we pushed the website into production in just 7-8 weeks as compared to 24-28 weeks. Though we published only a few limited features , but from the customers point of view , its a great ROI !

The second approach , can be vaguely called as the Agile Methodology , and Scrum is one of the frameworks to implement this methodology. There are many other frameworks which follow the Agile methodology like XP (eXtreme Programing),

Its worth noting that, the Agile is here not to replace Waterfall SDLC. But, to improve the process of execution or the process of development and testing. Instead of doing everything at one time, we simply break-down our work and complete it into phases. After a few phases, we publish a release and multiple such releases will gradually put the entire application into production.

#### Understanding Scrum

Scrum framework is surrounded by certain rules which must be followed to execute the development and testing phase of the project.Below are some key aspects of the Scrum framework which are essential for execution.

Scrum requires to have three roles viz...

1. Product Owner
2. Scrum Master
3. Development Team

Also, the framework mandates to maintain a document called "Product Backlog". The Product backlog contains a list requirements that needs to be implemented for this Project.

The Product Owner , is the Single Point of Contact for all the stakeholders of the project and decides what are the requirements. Maintaining the product backlog is the sole responsibility of the Product Owner. The Product Owner sits with the Development Team and decides which requirements he requires to be implemented in each sprint.

Scrum Master , facilitates the execution of the Scrum framework. He doesn't code, nor does he have any say in the requirements. He guides the Development team in following the scrum framework and interacts with the external world For Ex : if someone from the Dev team requires a new laptop, its the Scrum Masters responsibility to provide that , raise a request, follow for the POs etc.. its all done by Scrum Master. Apart from the admin jobs, The Scrum Master also shields the Dev team from other teams or other people to avoid multi-tasking of the resources in the Dev Team and ensures that they are focused in the current sprint and free from all distractions.

Dev Team , this is the heterogeneous team of developers,testers ,Business Analysts and designers. They work together and decide amongst themselves what work needs to be done. This team needs to meet everyday for 15 minutes and discuss the following points

1. Whats completed
2. What needs to be done
3. Are there are stucks ?

This 15 minute long meeting needs to be short and crisp.

Few points that must be kept in mind (which will be driven by the Scrum Master also) is that , a Sprint cannot exceed more than 4 weeks and a Dev team has to be between 4-9 people.

In the initiation phase the Product owner lists down all the requirements in a bullet point format , and creates the Product Backlog. The PO and The dev team sit together and decide how many Sprints would be required to complete all the requirements. This is just a high level estimation. After this the first Sprint starts with an expectation of completing 20 requirements. At the end of the sprint , the development team meets with he Product owner and shows the product to him. He reviews the product and gives his feedback and this continues for all the upcoming sprints.

If the team is unable to deliver the requirements in a particular sprint , then the remaining requirements go back to the backlog and will be considered in the next sprint.

Some aspects about Scrum which might be challenging for an organisation who is moving form Waterfall SDLC.

1. In Scrum,when the sprint starts, for lets say 3 weeks, no new requirement will be entertained. This requirement of the scrum will be really difficult in an environment where requirements keep changing.
2. The Product owner takes full responsibility and accountability for the requirements. This is again a big challenge as a single person taking full responsibility and accountability will be difficult to find.
3. Scrum Master and Product Owner roles cannot be managed by a single person.
4. The resources in the development team cannot be assigned to different projects and must focus on the current sprint only. Agile-Scrum is a mature framework and it strongly agrees with the fact that multi-tasking is not a correct approach as it heavily impacts the Quality of the product.
5. The Product Owner,Dev Team and the Scrum Master must meet very often or probably every after sprint to review the work done and provide feedback to improve themselves so that the same mistakes are not repeated in the upcoming sprints. The Dev team must meet everyday for 15 minutes and discuss their issues. So , one needs to understand is that communication is a must amongst the team and business owners. Its the key to success of the product. The current Waterfall SDLC lacks this aspect and everybody just ends up working in silos. This would be quite a challenging task for someone to move from waterfall sdlc to Agile

People often ask , so since we are using Agile , we dont need to go for all those boring documentation right ? 

Answer is WRONG !

By adapting Agile you are not freeing yourself of the responsibility to document stuff. Infact in Scrum , there is a document called Product Backlog , which needs to be updated after every sprint. 

To summarize , Agile-Scrum is more of a common-sensical approach to Project Management and Software development process wherein we must focus more on whats done and adapt as per the feedback received. This needs to be done in small iterations and develop your product piece by piece.

IMO , this particular methodology was adopted to bring the development team closer with the business team rather than making them work in silos. For Ex : Scrum mandates a daily meeting, which rarely is followed and practices across organisations big and small.

So a smoother communication (which is now enforced by Scrum methodology) is the key to success of an Agile process.