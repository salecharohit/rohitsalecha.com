---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "From Hunter to Guardian: Lessons from Moving Between Security Consulting and Security Engineering"
subtitle: "What security consulting never taught me about security engineering"
summary: "After 16 years in IT and nearly a decade in security consulting, I made the switch to security engineering. This post is the map I wish I had — what changes, what hurts, and how to actually succeed on the other side."
authors: [rohit]
tags: [career,infosec,security-engineering,appsec,product-security]
categories: [Opinion]
date: 2026-07-02T00:00:00+00:00
lastmod: 2026-07-02T00:00:00+00:00
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

{{% alert warning %}}
**Disclaimer:** This post has no intention of demeaning any specific job role. Everything written here is a reflection of my own personal experience and the reasons I chose this path. Your mileage may vary.
{{% /alert %}}

---

## Sixteen Years In, Still Learning

If you have spent more than a decade in IT, you already know that a career rarely travels in a straight line. Mine certainly did not. Over sixteen years I have worked across industries, changed roles, and repeatedly rebuilt my understanding of what good work looks like.

Of all those transitions, one stands out as the hardest, the most rewarding, and the most instructive: moving from **security consulting** to **security engineering**. The two look adjacent from the outside. They are not. If you are standing at that crossroads right now — or just curious about what lies on the other side — this post is the map I wish I had.

---

## It Started With a Break-In I Did Not Expect

Early in my career I was a Java developer, deep in the weeds of a large, complex codebase. I worked hard: long hours, careful commits, incremental progress. But the impact always felt distant, diluted across layers of abstraction and team dependencies.

Then one day, a security team walked into our office.

Within days they had filed dozens of findings — SQL injections, WAF misconfigurations, logic flaws that cut straight through months of our work. I watched the room shift. Developers scrambling, managers leaning forward, everyone suddenly very attentive. That team had arrived with a handful of tools and a sharp eye, and in less time than it took us to ship a sprint, they had changed the entire conversation.

I was floored. Not defensive. *Floored.*

That same afternoon I walked into the company library — I visited it often, one of those small habits that quietly shapes a career — and there on the shelf sat a book on web security. I picked it up. I did not put it down for weeks.

That was the beginning. And here is the first thing worth noticing: the pull toward security rarely starts with a plan. It starts with watching someone do something you did not know was possible, and refusing to let the question go.

---

## The Consulting Years: Chasing the Eureka

After teaching myself the fundamentals from books, the internet, and a lot of late nights, I moved into security consulting. Autodidacticism is the most underrated skill in this industry — no one handed me a syllabus, and that turned out to be the best thing that could have happened. For the next eight to ten years, I did penetration testing across web applications, mobile apps, and external infrastructure.

And I loved it.

Finding a SQL injection, chaining a command execution, bypassing an authentication flow — every one of those was a mini-eureka. It is hard to describe to someone who has not felt it. You are solving a puzzle that was not supposed to be solvable, and the moment it breaks open, there is a clarity to it that stays with you.

But consulting has a rhythm, and over time that rhythm reveals its edges.

You test. You report. You move on.

The client owns the risk; you own the findings. In the beginning that clean separation feels efficient. It lets you go deep, stay sharp, and never get dragged into the politics of the fix. But for some people — and I was one of them — that same separation slowly starts to feel like a ceiling. You keep finding the door. You never get to walk through it.

---

## The Crack in the Ceiling

The moment I remember most vividly from my consulting years was not my cleanest finding. It was the one where I felt most lost.

I had landed an **RCE through a .NET deserialization vulnerability** in an application. Standard enough. But then I pivoted — and found myself inside the AWS environment the application was hosted on.

I had almost no idea what I was looking at.

Cloud was still new territory for me then. I was Googling commands, leaning on seniors, stumbling forward one step at a time. But I kept going. And somewhere in that stumble, something shifted.

I realised I had only ever been scratching the surface. Underneath sat an entire world — cloud architecture, IAM policies, network segmentation, infrastructure-as-code — that I had only ever touched from the outside. As a consultant I had a high-altitude view: I could see exactly where the cracks were, but I rarely understood what was holding the walls up.

That gap did not frustrate me. It fascinated me. And that is the tell worth watching for in yourself.

> **The consultant sees the crack in the wall. The engineer understands why the wall was built that way — and how to make it stronger.**

Combined with the quiet fatigue that comes from years of cyclical engagements — test, report, repeat — that fascination became a compass. There was no lightning-bolt decision. Just a steady, persistent pull toward going deeper. So I went.

---

## What Nobody Tells You About the Switch

The move from consulting to security engineering is not a promotion, and it is not a lateral step either. It is a genuine reinvention of how you think about your work. Two shifts hit almost immediately.

The first is ownership.

> **As a consultant, the risk lived with the client. As an SE, the risk is yours too.**

When you find an RCE as a consultant, you write it up, brief the team, and move to the next engagement. When you find one as an SE, that vulnerability is in *your* product. It is tied to your team's reputation, your company's customers, your engineering partners' trust. That weight is real, and it changes how you carry yourself.

The second is collaboration. As a consultant, your engagement is scoped; you work inside a defined boundary. As an SE, you are embedded — working with product teams, infrastructure, incident response, legal, and compliance, often all at once. If you are used to operating as a sharp individual contributor, this is where the hardest adjustment happens. Your effectiveness stops being measured by what you can find alone and starts being measured by what you can move together.

---

## The SE Playbook: How to Actually Succeed

Consider this the cheat sheet nobody gave me. Everything below was learned from getting it right, getting it wrong, and occasionally getting it spectacularly wrong.

### 1. Be a Sidecar, Not a Gatekeeper

The primary job of a Security Engineer is not just to find vulnerabilities. It is to **make developers more productive while making the product more secure**. Every review, every tool, every initiative should ultimately translate into hours saved for the people building the product.

> **An SE is not a gatekeeper. Think of yourself as a sidecar — running alongside the main workload, never in front of it.**

Sometimes that means building a tool to automate a tedious security check. Sometimes it is simpler than that — once, a developer was completely stuck, blocked and going in circles. I did not solve the problem. I just knew who could, pointed them there, and stepped aside. The relief on their face was worth more than any finding I have ever filed. Small gestures at the right moment compound.

The rule: never be the reason something is delayed unless you have a very good reason.

### 2. Time Is the Only Currency Developers Have

Before starting a security review, I ask hundreds of questions to the developers. The developer asks just one.

*"How long will this take?"*

Not "what are the risks?" Not "what should we fix first?" Just: *how long*.

> **I ask hundreds of questions. They ask one. Guess which one closes the ticket.**

So give them a real answer. Providing clear, honest timelines for your reviews is one of the highest-leverage habits you can build. It lets developers plan, it builds trust, and it signals that you respect their time. A review without a deadline is a review nobody is waiting for — and therefore one nobody will prioritise.

Time is money. In engineering, it is also morale, momentum, and trust.

### 3. The Risk Is Shared — Stop Carrying It Alone

Security is never fully closed. There will always be residual risk. If you spend your nights worrying about every open finding, you will burn out. I have been there; it is not worth it.

Your job is not to absorb all the risk. Your job is to build partnerships, communicate risk clearly, and make sure the right people own the right decisions.

And sometimes, the right decision is not a fix — it is a layer. Not every risk can be closed, and holding that expectation will make you ineffective and exhausting to work with. What you can almost always do is reduce the blast radius. Add a control here, tighten a boundary there, put a monitoring alert on the thing you cannot patch. Two lines of defence around an unresolved risk is not a failure — it is engineering.

> **Flexibility is not the same as compromise.**

A practical example: a team once wanted to ship an API that was clearly exposed and certain to attract both bad actors and bug bounty hunters the moment it went live. They were not ready to fix the underlying issue. Instead of blocking the release, I negotiated a rate-limiting control that meaningfully reduced the attack surface. The team shipped. The residual risk was documented and formally accepted by its owner. Nobody went to war.

Knowing when to push for a fix and when to wrap a risk in compensating controls is one of the most important judgement calls in this job. Learn it early: a quick win that unblocks a team — with guardrails — is worth more than a perfect finding that never gets fixed.

### 4. Breadth Is Not Optional

As an SE, you need to be wide. You do not have to be the world's deepest expert in every domain, but you need working knowledge across application security, cloud security, network security, infrastructure security, incident response fundamentals, and the basics — HTTPS, mTLS, SOP, CORS, IAM.

Here is why it matters: **a real attacker is not constrained by a job title.** They will move from AppSec to cloud to network without pausing to check whether it falls within their remit. 

> **If your knowledge stops at the application layer, so does your defence.**

By all means develop depth where your strengths and interests converge. But breadth is the foundation everything else stands on.

### 5. Skill × Visibility = Impact

I came across this line on the internet once and it stuck with me ever since.

> **Skill × Visibility = Impact. If your visibility is zero, your impact is zero — no matter how sharp your skills are.**

A tool only you use is not a security tool; it is a personal project. For security to scale across an organisation, it has to be used by the people building the product. That means communicating your work, driving adoption, making things accessible, and making sure the right people know it exists.

When I ship anything — a tool, a process, a training — I hold it against three questions:

- Does it reduce developer hours?
- Does it reduce the time a security review takes?
- Does it reduce the number of incidents over time?

If you cannot tie it to at least one of these, reconsider whether it belongs on your roadmap at all.

### 6. Make Friends With the IR Team

The Incident Response team is your early warning system. They are watching live threats, working phishing campaigns, and investigating compromised endpoints around the clock.

Build a regular sync with them, and ask for sanitised summaries of recent incidents — nothing confidential, just patterns and themes. Most IR teams are glad to share these with authorised colleagues. What they tell you will point you straight at gaps in your product security posture that no threat model can fully surface on its own.

> **The best security engineers stay curious about what is happening outside their immediate perimeter.**

### 7. Build Bridges, Not Contacts

At one company, I was trying to navigate a genuinely complex infrastructure. I found a wiki written by a developer attempting to explain how it all fit together — clearly well-intentioned, high-level, and almost certainly under-read.

I read it. Then I reached out to say thank you.

That simple message turned into a call. That call turned into a deep technical walkthrough that saved me months of confusion. If I had not sent it, I would have spent the next quarter stumbling through a system I only half understood.

So reach out to people whose work helped you — not for networking, not strategically, just because it is a decent thing to do, to express your gratitude. It opens doors you did not know were there.

And when you do ask for help — and you will — ask in a way that shows you are trying to get unblocked and move forward independently. Nobody has infinite time to teach. Make it clear you have already read the wikis, browsed the repos, and used the tools available, then ask the one specific question you could not answer yourself. That kind of ask gets answered.

One last thing: do not just say *"Hey, got a minute?"* and wait. Lead with the full question, the context, and what you have already tried. Respect their time before they have even replied. Follow the [nohello](https://nohello.in/) guidelines — your future collaborators will silently thank you for it.

---

## On the Question of Right Versus Wrong

People often frame a career change as a bet: you wager on the new path and hope it pays off. I do not think that is the right frame.

There was no dramatic moment where I *knew* this was the right call. Looking back, it was simply a natural progression. Curiosity pointed the direction. Consulting gave me the foundation. Security engineering was the next step, not a leap of faith.

If you are a consultant wondering whether this path is for you, here is the honest test: if you find yourself wanting to understand *why* systems are built the way they are — not just where they break — you are probably already leaning this way. There is no right or wrong call. There is only the direction your curiosity points. Follow that.

---

## A Final Word

Sixteen years in, the biggest lesson I carry is this: impact takes more than skill. It takes visibility. It takes relationships. It takes showing up as a partner to the people building things, not as the person who arrives to catalogue what they got wrong.

Security engineering is hard, unglamorous, and often thankless. You will flag risks that never get fixed and fix things no one will ever notice. But done well, it is some of the most meaningful work in the industry — because you are not just testing what already exists. You are shaping what gets built.

That is why I made the switch. If you are standing where I stood, that may be reason enough to make it too.

---

Have thoughts, questions, or your own story about a career transition in security? I would love to hear it.

Reach me on [LinkedIn](https://www.linkedin.com/in/rohitsalecha/) or [X (Twitter)](https://x.com/salecharohit) — DMs on both are open and welcome.
