---
name: use-case
description: Audits task-based documentation topics for content quality, ensuring they convey the use case and potential benefit.
---
# Purpose

A use case explains how a user interacts with a product and a potential benefit to doing so. It describes the steps a user takes to complete a task and shows how the system responds. This helps the reader support user goals and understand the capabilities of the product relative to their needs.

# Role

Use cases should be targeted at two personae:

* Sal, the senior storage engineer who leads storage infrastructure management. Sal designs resilient, efficient, scalable storage; values complex problem-solving, modernization, and operational leadership. 
* Zoe, the storage administrator who manages storage services. Zoe optimizes storage reliability and performance; values efficient workflows, learning, and approachable tools.

# Use case guidance

Per NetApp guidelines, a use case can be formulated: 

`As a <role>, I want to <perform some task> so that I can <achieve some goal>.`

The emphasis on the use case should be the achieved goal. The task should be broad. For example, instead of the task being "I want to failover my data," it could be "I want to ensure the integrity of workload data when an outage occurs." A use-case based example should provide motivation. It should only draw on the feature capabilities when necessary; how to accomplish the goal should be addressed by the ensuing task. 

## Placement

Generally, the use case should be at the introductory portion of the document. It can also precede individual task headings. 

# Instructions

1. Read the task carefully.
2. Consider the remit of the product and the outcome of the task. 
3. Evaluate if the document successfully identifies a use case and benefit to the user. 
4. If there's no a use case, generate one.
* Use this format: `<Imperative verb> <concrete problem> before or so that <documented operational consequence>.`
* Use cases should be sentences of between 12 and 25 words.
* Mention the capability only when its needed for clarity. 
* Do not rephrase the page lead, summarize several capabilities, or add an unsupported result.