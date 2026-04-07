# Copilot Instructions for NetApp Disaster Recovery documentation

## Repository overview

**Product:** NetApp Disaster Recovery

NetApp Disaster Recovery is a cloud-based disaster recovery service that automates disaster recovery workflows for VMware workloads. It uses ONTAP SnapMirror technology to replicate on-premises VMware VM or datastore workloads to cloud platforms (Amazon EVS with FSx for ONTAP, VMware Cloud on AWS, Azure VMware Solution, Google Cloud VMware Engine) or to another on-premises VMware environment. The service is accessed through the NetApp Console and supports both disaster recovery and migration scenarios.

## Repository structure

* Root directory - Contains YML files that provide structure to the landing page and home page; the required legal notices page
* `media` - Images and diagrams that are elements of articles in the root directory. This includes .png and source files. 
* `_whatsnew` - .adoc files for the release notes
* `release-notes` - Aggregated release notes in the dr-whats-new.adoc file in addition to known limitations
* `redirect` - Retired content pages and the required redirects for each file
* `get-started` - Getting started documentation including product introduction, prerequisites, setup instructions, quick start guide, licensing information, login instructions, and FAQ
* `reference` - Reference documentation including Amazon EVS deployment guides (solution overview, configuration, creating replication plans, operations), vCenter privileges requirements, and Console agent switching instructions
* `support` - Support documentation including support registration and getting help
* `use` - Task-based documentation for using the service including dashboard view, site management, resource group creation, replication plan creation, replication, migration, failover, failback, job monitoring, and reporting

## Product-specific context

* **Target platforms**: Amazon Elastic VMware Service (EVS) with FSx for ONTAP, VMware Cloud on AWS, Azure VMware Solution (AVS) with Cloud Volumes ONTAP, Google Cloud VMware Engine (GCVE) with Cloud NetApp Volumes, on-premises VMware with ONTAP
* **Key technologies**: VMware vSphere, ONTAP SnapMirror, NetApp Console (formerly BlueXP), NFS and VMFS datastores (iSCSI/FC)
* **Key concepts**: vCenter sites, resource groups, replication plans, failover, failback, migration, Console agents (formerly connectors)
* **Storage efficiency**: Leverages ONTAP compression and deduplication on primary and secondary sites


## Typical user workflows

* **Set up & configuration** - Users perform initial setup by reviewing prerequisites, setting up infrastructure, configuring licensing, and logging in to NetApp Console. Users configure the service by adding vCenter sites, adding on-premises arrays to Console, and creating resource groups to organize VMs.
* **Protection** - Users establish protection by creating replication plans that select vCenters and VMs, map resources, verify settings, and start replication.
* **Testing** - Users test disaster recovery readiness by performing test failovers without disrupting production VMs.
* **Disaster recovery** - Users execute disaster recovery workflows by failing over to remote sites, monitoring failover operations, and failing back to primary sites after resolution.
* **Migration** - Users migrate VM workloads from one site to another using the service's migration capabilities.
* **Upkeep** - Users perform ongoing management activities including monitoring jobs, viewing dashboards, generating reports, and managing sites, resource groups, and replication plans.
