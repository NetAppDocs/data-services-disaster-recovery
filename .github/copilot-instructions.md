# Copilot Instructions for NetApp Disaster Recovery documentation

## Repository overview

**Product:** NetApp Disaster Recovery

NetApp Disaster Recovery is a cloud-based service in the NetApp Console that protects on-premises and cloud-hosted VMware and Kubernetes workloads. It automates replication, test failover, failover, failback, and migration workflows using ONTAP SnapMirror technology. The service is accessed through the NetApp Console and supports both disaster recovery and migration scenarios.

## Repository structure

* `_include` - Reusable text blocks that capture pieces of information reused across the site (such as Console permission requirements); use these to create a single source of truth
* `_whatsnew` - .adoc files for the release notes
* `get-started` - Getting started documentation including product introduction, prerequisites, setup instructions, quick start guide, licensing information, login instructions, and FAQ
* `media` - Images and diagrams that are elements of articles in the root directory. This includes .png and source files.
* `redirect` - Retired content pages and the required redirects for each file
* `release-notes` - Aggregated release notes in dr-whats-new.adoc, along with known limitations
* `reference` - Reference documentation including Amazon EVS deployment guides (solution overview, configuration, creating replication plans, operations), vCenter permissions requirements, and Console agent switching 
* `support` - Support documentation including support registration and getting help
* `use` - Task-based documentation for using the service including dashboard view, site management, resource group creation, replication plan creation, replication, migration, failover, failback, job monitoring, and reporting

## Product-specific context

- *NetApp Disaster Recovery* is the official product name.
  - Use the full name, "NetApp Disaster Recovery," in every H1 and in the first product reference after the `[.lead]` paragraph marker.
  - After that first use, use only "Disaster Recovery" for every subsequent reference in the topic. This includes H2 and lower headings, link text, UI menu names (for example, "From the Disaster Recovery menu"), and image alt text.
  - Do not shorten the name in front matter (`keywords` and `summary`).
  - Generic lowercase "disaster recovery" (the concept, not the product) is not the product name. Leave it as is.
  - Do not apply these product name rules to files in the `_include`, `_whatsnew`, or `redirect` directories.
- *Resource group* is the logical unit of protection (VMs, datastores, or Kubernetes resources) and is the object assigned to a replication plan.
- *Replication plan* defines source/target mappings, schedule, retention, recovery mappings, and operations such as replicate, failover, and failback.
- *SnapMirror* is the replication transport; protection is volume/LUN based even when users select VMs or datastores in the UI.
- *Test failover* creates temporary recovery artifacts (including FlexClone-backed datastores) to validate recovery without disrupting production workloads.
- *Subnet mapping* preserves host bits and remaps network portions during failover IP reassignment.
* *Console agent* - NetApp component that ensures connectivity between on-premises storage systems and NetApp data services in the cloud.
* *Storage VM* - an isolated, logical file/storage server running inside a NetApp ONTAP cluster that serves data to clients. Use "storage VM" in the first instance with the abbreviation (SVM). Subsequent uses can include SVM. Do not use vServer. 
* *Resource* - This is not a technical term but should be used as a generic reference when referring to data resources such as datastores, VMs, or Kubernetes. Use only for references that span workload types (that is, Kubernetes and VMware)

## Typical user workflows

* **Set up & configuration** - Users perform initial setup by reviewing prerequisites, configuring licensing & infrastructure, and logging in to NetApp Console. Users configure the service by adding vCenter or Kubernetes sites, adding on-premises arrays to Console, and creating resource groups to organize VMs.
* **Protection** - Users establish protection by creating replication plans that select vCenters and VMs, map resources, verify settings, and start replication.
* **Testing** - Users test disaster recovery readiness by performing test failovers without disrupting production VMs.
* **Disaster recovery** - Users execute disaster recovery workflows by failing over to remote sites, monitoring failover operations, and then failing back to primary sites after resolution.
* **Migration** - Users migrate VM workloads from one site to another using the service's migration capabilities.
* **Maintenance** - Users perform ongoing management activities including monitoring jobs, viewing dashboards, generating reports, and managing sites, resource groups, and replication plans.
