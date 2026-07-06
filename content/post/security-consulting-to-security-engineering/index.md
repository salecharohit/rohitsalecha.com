---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "What I Learned Moving from Security Consulting to Security Engineering"
subtitle: "A decade in security consulting, and what changed when I crossed over to engineering"
summary: "After 16 years in IT and nearly a decade in security consulting, I moved into security engineering. This post is the map I wish I had — what changes, what stays with you, and how the consultant's eye turns out to be the best thing you bring."
authors: [rohit]
tags: [career,infosec,security-engineering,appsec,product-security]
categories: [Opinion]
date: 2026-07-02T00:00:00+00:00
lastmod: 2026-07-06T00:00:00+00:00
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

{{% alert note %}}
Everything here is my own experience and the reasons I chose this path. Consulting and engineering are two different crafts, not two rungs of a ladder — plenty of brilliant people do either for life. Your mileage may vary.
{{% /alert %}}

---

## Sixteen Years In, Still Learning

Over sixteen years in IT I have changed roles more than once, but one move stands out as the hardest and most instructive: from **security consulting** to **security engineering**. The two look adjacent from the outside. They are not — they are two different crafts, breaking and building, aimed at the same goal from opposite sides.

Here is the idea this whole post rests on: **I did not graduate out of consulting into engineering. I carried the consultant's eye across the fence — and it turned out to be the most valuable thing I brought.**

If you are standing at that crossroads, this is the map I wish I had. The first half is how I got here; the second half — [the SE playbook](#the-se-playbook-how-to-actually-succeed) — is seven hard-won rules about shipping security inside a product team. Short on time? Skip ahead to it.

---

## It Started With a Break-In I Did Not Expect

Early in my career I was a Java developer, deep in a large codebase, working hard but rarely feeling the impact — it was diluted across layers of abstraction and team dependencies. Then one day a security team walked into our office.

Within days they had filed dozens of findings — SQL injections, WAF misconfigurations, logic flaws that cut straight through months of our work. In less time than it took us to ship a sprint, they had changed the entire conversation. I was floored. Not defensive. *Floored.*

That same afternoon I found a book on web security in the company library and did not put it down for weeks. That is how it starts for most people: not with a plan, but with watching someone do something you did not know was possible, and refusing to let the question go.

---

## The Consulting Years: Chasing the Eureka

After teaching myself the fundamentals — no one handed me a syllabus, which turned out to be the best thing that could have happened — I moved into security consulting. For the next eight to ten years I did penetration testing across web, mobile, and external infrastructure. And I loved it. Finding a SQL injection, chaining a command execution, bypassing an authentication flow — every one was a mini-eureka: a puzzle that was not supposed to be solvable, breaking open with a clarity that stays with you.

But consulting has a rhythm — you test, you report, you move on. The client owns the risk; you own the findings. That clean separation is not a flaw, it is the whole point: it lets you go deep, stay sharp, and skip the politics of the fix. Plenty of exceptional people build entire careers on exactly that focus. But it is a boundary, and some people get restless standing behind it. I was one of them. I kept finding the door. I wanted to walk through it.

---

## The Door I Wanted to Walk Through

The moment I remember most vividly from my consulting years was not my cleanest finding — it was the one where I felt most lost. I had landed an **RCE through a .NET deserialization vulnerability**, then pivoted and found myself inside the AWS environment the application was hosted on. I had almost no idea what I was looking at.

Cloud was still new territory for me. I Googled commands, leaned on seniors, stumbled forward — and somewhere in that stumble, something shifted. There was an entire world beneath the one I had been paid to test — cloud architecture, IAM, network segmentation, infrastructure-as-code — a whole board I had only ever played from one side. I could find my way in; what I could not yet see was why the system had been built that way, or how it held together under the surface. I did not want to trade one view for the other. I wanted both.

That appetite did not frustrate me. It fascinated me — and that is the tell worth watching for in yourself.

There was no lightning-bolt decision, just a steady pull toward owning the whole board instead of half of it. So I went — not away from consulting, but toward the part of the game I had not played yet.

---

## What Nobody Tells You About the Switch

The move is not a promotion, and not a lateral step either. What surprised me most: the thing that changes is not *how hard you think* — consulting was every bit as demanding — it is **what you are responsible for, and who you are responsible to.** Two shifts hit immediately.

The first is ownership.

> **As a consultant, the risk lived with the client. As an SE, the risk is yours too.**

Find an RCE as a consultant and you write it up, brief the team, and move to the next engagement. Find one as an SE and that vulnerability is in *your* product — tied to your team's reputation, your customers, your partners' trust. That weight is real, and it changes how you carry yourself.

The second is collaboration. A consulting engagement is scoped; as an SE you are embedded — working with product, infrastructure, incident response, legal, and compliance, often at once. If you are used to operating as a sharp individual contributor, this is the hardest adjustment: your effectiveness stops being what you can find alone and starts being what you can move together.

---

## The SE Playbook: How to Actually Succeed

Consider this the cheat sheet nobody gave me. Everything below was learned from getting it right, getting it wrong, and occasionally getting it spectacularly wrong.

### 1. Be a Sidecar, Not a Gatekeeper

The primary job of a Security Engineer is not just to find vulnerabilities. It is to **make developers more productive while making the product more secure**. Every review, every tool, every initiative should ultimately translate into hours saved for the people building the product.

> **An SE is not a gatekeeper. Think of yourself as a sidecar — running alongside the main workload, never in front of it.**

Sometimes that means building a tool to automate a tedious security check. Sometimes it is simpler than that — once, a developer was completely stuck, blocked and going in circles. I did not solve the problem. I just knew who could, pointed them there, and stepped aside. The relief on their face was worth more than any finding I have ever filed. Small gestures at the right moment compound.

### 2. Time Is the Only Currency Developers Have

Before starting a security review, I ask the developers dozens of questions. The developer asks just one.

*"How long will this take?"*

Not "what are the risks?" Not "what should we fix first?" Just: *how long*.

> **I ask dozens of questions. They ask one. Guess which one closes the ticket.**

So give them a real answer. Providing clear, honest timelines for your reviews is one of the highest-leverage habits you can build. It lets developers plan, it earns their confidence, and it signals that you respect their time. A review without a deadline is a review nobody is waiting for — and therefore one nobody will prioritise.

In engineering, time is not just money — it is morale, momentum, and trust.

### 3. The Risk Is Shared — Stop Carrying It Alone

Security is never fully closed. There will always be residual risk. If you spend your nights worrying about every open finding, you will burn out. I have been there; it is not worth it.

Your job is not to absorb all the risk. Your job is to build partnerships, communicate risk clearly, and make sure the right people own the right decisions.

And sometimes, the right decision is not a fix — it is a layer. Not every risk can be closed, and holding that expectation will make you ineffective and exhausting to work with. What you can almost always do is reduce the blast radius. Add a control here, tighten a boundary there, put a monitoring alert on the thing you cannot patch. Two lines of defence around an unresolved risk is not a failure — it is engineering.

> **Flexibility is not the same as compromise.**

A practical example: a team once wanted to ship an API that was clearly exposed and certain to attract both bad actors and bug bounty hunters the moment it went live. They were not ready to fix the underlying issue. Instead of blocking the release, I negotiated a rate-limiting control that meaningfully reduced the attack surface. The team shipped. The residual risk was documented and formally accepted by its owner. Nobody went to war.

Knowing when to push for a fix and when to wrap a risk in compensating controls is one of the most important judgement calls in this job. Learn it early: a quick win that unblocks a team — with guardrails — is worth more than a perfect finding that never gets fixed.

### 4. Breadth Is Not Optional

As an SE, you need to be wide. You do not have to be the world's deepest expert in every domain, but you need working knowledge across application security, cloud security, network security, infrastructure security, incident response fundamentals, and the basics — HTTPS, mTLS, Same-Origin Policy, CORS, IAM, and networking up and down the OSI stack, from DNS and TLS at the top to TCP/IP and packets on the wire at the bottom.

Here is why it matters: **a real attacker is not constrained by a job title.** They will move from AppSec to cloud to network without pausing to check whether it falls within their remit.

> **If your knowledge stops at the application layer, so does your defence.**

This is exactly where the consulting years pay off. I already thought like an attacker who ignores boundaries — that was the job. Engineering just asked me to defend the same way I used to attack: across every layer, not one at a time. By all means develop depth where your strengths and interests converge. But breadth is the foundation everything else stands on.

### 5. Skill × Visibility = Impact

I came across this line on the internet once and it stuck with me.

> **Skill × Visibility = Impact. If your visibility is zero, your impact is zero — no matter how sharp your skills are.**

A tool only you use is not a security tool; it is a personal project. For security to scale across an organisation, it has to be used by the people building the product. That means communicating your work, driving adoption, making things accessible, and making sure the right people know it exists.

When I ship anything — a tool, a process, a training — I hold it against three questions:

- Does it reduce developer hours?
- Does it reduce the time a security review takes?
- Does it reduce the number of incidents over time?

If you cannot tie it to at least one of these, reconsider whether it belongs on your roadmap at all.

### 6. Make Friends With the IR Team

The Incident Response team is your early warning system. They are watching live threats, working phishing campaigns, and investigating compromised endpoints around the clock.

Build a regular sync with them, and ask for sanitised summaries of recent incidents — nothing confidential, just patterns and themes. How much they can share depends on your org: in mature teams this is routine, while in stricter environments IR sits behind need-to-know walls and you will get less. Ask anyway, respect the boundary, and take whatever patterns you can get. What they tell you will point you straight at gaps in your product security posture that no threat model can fully surface on its own.

> **The best security engineers stay curious about what is happening outside their immediate perimeter.**

### 7. Build Bridges, Not Contacts

At one company, I was trying to navigate a genuinely complex infrastructure. I found a wiki written by a developer attempting to explain how it all fit together — clearly well-intentioned, high-level, and almost certainly under-read.

I read it. Then I reached out to say thank you.

That simple message turned into a call. That call turned into a deep technical walkthrough that saved me months of confusion. If I had not sent it, I would have spent the next quarter stumbling through a system I only half understood.

So reach out to people whose work helped you — not for networking, not for leverage, just because it is a decent thing to do, to express your gratitude. It opens doors you did not know were there.

And when you do ask for help — and you will — earn it first. Do the research before you reach out: read the wikis, browse the repos, try the tools. Then ask the one specific question you genuinely could not answer on your own. Nobody has infinite time to teach, and nobody owes you spoon-feeding. An ask that shows you have already done the work gets answered; an ask that outsources the work gets ignored.

One last thing: do not just say *"Hey, got a minute?"* and wait. Lead with the full question, the context, and what you have already tried. Respect their time before they have even replied. Follow the [nohello](https://nohello.in/) guidelines — your future collaborators will silently thank you for it.

---

## A Final Word

Sixteen years in, the biggest lesson I carry is this: impact takes more than skill. It takes visibility. It takes relationships. It takes showing up as a partner to the people building things, not as the person who arrives to catalogue what they got wrong.

Security engineering is hard, unglamorous, and often thankless. You will flag risks that never get fixed and fix things no one will ever notice. But done well, it is some of the most meaningful work in the industry — because you are not just testing what already exists. You are shaping what gets built. And you shape it best when you never lose the instinct that let you break things in the first place.

If you are a consultant wondering whether this path is for you, here is the honest test: if you find yourself wanting to understand *why* systems are built the way they are — not just where they break — you are probably already leaning this way. And if you make the move, know this: you are not starting over. You are bringing the best of one craft into another.

That is why I made the move — not to leave one craft, but to fuse it with another. If you are standing where I stood, that may be reason enough to make it too.

---

Have thoughts, questions, or your own story about a career transition in security? I would love to hear it.

Reach me on [LinkedIn](https://www.linkedin.com/in/rohitsalecha/) or [X (Twitter)](https://x.com/salecharohit) — DMs on both are open and welcome.
