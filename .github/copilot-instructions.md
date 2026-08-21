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

- *Resource group* is the logical unit of protection (VMs, datastores, or Kubernetes resources) and is the object assigned to a replication plan.
- *Replication plan* defines source/target mappings, schedule, retention, recovery mappings, and operations such as replicate, failover, and failback.
- *SnapMirror* is the replication transport; protection is volume/LUN based even when users select VMs or datastores in the UI.
- *Test failover* creates temporary recovery artifacts (including FlexClone-backed datastores) to validate recovery without disrupting production workloads.
- *Subnet mapping* preserves host bits and remaps network portions during failover IP reassignment.


## Typical user workflows

* **Set up & configuration** - Users perform initial setup by reviewing prerequisites, configuring licensing & infrastructure, and logging in to NetApp Console. Users configure the service by adding vCenter or Kubernetes sites, adding on-premises arrays to Console, and creating resource groups to organize VMs.
* **Protection** - Users establish protection by creating replication plans that select vCenters and VMs, map resources, verify settings, and start replication.
* **Testing** - Users test disaster recovery readiness by performing test failovers without disrupting production VMs.
* **Disaster recovery** - Users execute disaster recovery workflows by failing over to remote sites, monitoring failover operations, and then failing back to primary sites after resolution.
* **Migration** - Users migrate VM workloads from one site to another using the service's migration capabilities.
* **Maintenance** - Users perform ongoing management activities including monitoring jobs, viewing dashboards, generating reports, and managing sites, resource groups, and replication plans.
