---
name: use-case
description: Audits task-based documentation topics for content quality, ensuring they convey the use case and potential benefit.
---
# Purpose

A use case states why a user performs a task and what they gain from doing so. It focuses on the user's goal, not the product feature. Use cases help readers quickly understand whether a topic is relevant to their situation and why the task matters.

In contrast, task-based documentation captures _how_ to do something. Feature based documentation captures _what_ the feature does. 

Use-case based documentation should capture the _how_, the _what_, and the _why_. 

Canonical source: https://review.docs.netapp.com/us-en/content-standards/use-cases/use-cases.html

# Audience

Use cases in this repository are written for two personas:

* **Sal**, a senior storage engineer who leads infrastructure planning and design. Sal values operational leadership, complex problem-solving, and modernization.
* **Zoe**, a storage administrator who manages day-to-day storage services. Zoe values efficient workflows, reliable tools, and clear guidance.

When evaluating a use case, consider whether it speaks to the goal of at least one of these personas.

# What makes a valid use case

A valid use case:

- States the user's problem or goal, not the product action
- Highlights the benefit of making the change, or the detriment of not
- Is grounded in what the page actually describes
- Is 12–25 words

A use case is not valid if it:

- Restates the page title or lead sentence
- Summarizes multiple capabilities
- Claims a benefit the page does not support
- Describes a product feature rather than a user need

# Format

Use this pattern when generating a use case:

`<Imperative verb> <concrete problem> before or so that <documented operational consequence>.`

Mention the product capability only when it is needed for clarity. Do not name features for their own sake.

**Example (weak):** "Use NetApp Disaster Recovery to create a replication plan so that you can replicate VMs."

**Example (strong):** "Define recovery mappings and boot behavior before a disaster so that workloads restart in the correct order at the target site."

## Placement

Place the use case at the start of the topic, within or just after the lead paragraph. It can also appear before an individual task heading when a section introduces a distinct workflow.

## Examples

A reliable use case should synthesize the feature or task description with a statement of the user value. Use these two exmaples:

* Example 1: Snapshot replication is a process in which consistency groups on your ASA r2 system are copied to a geographically remote location. After the initial replication, changes to consistency groups are copied to the remote location based upon a replication policy. Replicated consistency groups can be used for disaster recovery or data migration.

* Example 2: When you clone a consistency group, you create a new consistency group that's identical in structure, storage units, and data to the consistency group you cloned. Use a consistency group clone to perform application testing or to migrate data. Suppose, for example, you need to migrate a production workload out of a consistency group. You can clone the consistency group to create a copy of your production workload to maintain as a backup until the migration is complete.

# Instructions

1. Read the task topic carefully.
2. Identify the user's goal and the consequence of not completing the task.
3. Check whether the document states this goal explicitly — in the lead, a note, or a setup sentence.
4. Evaluate the use case against the criteria above.
5. If no valid use case is present, generate one using the format above.

## Output format

Return your review in this structure:

**Use case present:** Yes / No / Partial

**Assessment:** One or two sentences explaining why the use case is present, absent, or weak.

**Suggested use case:** (if absent or weak) A single sentence, 12–25 words, in the required format.

**Suggested revised introduction:** (if the use case is absent or weak) Synthesize the suggested use case with the existing introduction.