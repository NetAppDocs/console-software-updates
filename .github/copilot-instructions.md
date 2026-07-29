## Copilot instructions for Software updates documentation

### Repository overview
Product: Software updates

*Software updates* in *NetApp Console* helps users assess readiness, choose a target *ONTAP* version, and execute storage system updates. The content in this repository focuses on the Console workflow for ONTAP updates, related prerequisites, update execution paths, release notes, and support tasks.

### Repository structure
- `get-started/` – Introductory and access content for *software updates*, including overview, prerequisites, login, quick start, and FAQ pages.
- `ONTAP/` – Task content for the ONTAP update workflow, including version comparison, blocker handling, update initiation, and status validation.
- `support/` – Support and registration pages for *NetApp Console* that rely on shared included content.
- `release-notes/` – Published "what's new" page for the *software updates* service.
- `_whatsnew/` – Date-stamped source snippets included by `release-notes/whats-new.adoc`.

### Product-specific context
**Architecture and components:**
- *Software updates* is accessed from the *NetApp Console* left navigation under *Health* > *Software updates*.
- The workflow operates on *ONTAP storage systems* and their *clusters* and *nodes*; users identify a target version, review blockers and warnings, and initiate the update from the service.
- Some update paths complete inside *NetApp Console*, while other paths redirect users to *System Manager* for the actual ONTAP update.
- A *Console agent* enables in-Console ONTAP update execution for supported environments; without an agent, some clusters are updated through *System Manager* instead.
- Update history reflects processed *AutoSupport* data after the ONTAP version changes.

**Key concepts:**
- *Target version* is the ONTAP version selected for the storage system update; users can compare the recommended version or choose another available version.
- *Blockers* are issues that must be fixed and acknowledged before the update can continue; *warnings* are reviewed before proceeding.
- *Update plan* is the downloadable comparison output that summarizes feature benefits and risks for a selected target version.
- *Cluster discovery* requires the ONTAP cluster IP address and administrator credentials so the service can execute the update workflow.
- The service is not supported for *Cloud Volumes ONTAP* clusters or clusters in a *MetroCluster* configuration.

**Naming conventions and terminology:**
- Use *NetApp Console* as the platform name and *software updates* as the service name.
- Use *ONTAP*, *cluster*, *node*, *System Manager*, *Console agent*, *AutoSupport*, *blockers*, *warnings*, *History* tab, and *Target version* with their product-specific meanings from the UI and workflows in this repo.
- Access roles referenced in the repository include *Organization admin*, *Folder or project admin*, *Storage admin*, *Storage viewer*, and *System health specialist*.

### Typical user workflows
**Access the service:** Open *NetApp Console* → Log in with supported credentials → Select *Health* → Select *Software updates*

**Prepare and run an ONTAP update:** Review prerequisites → Discover or select the target cluster → Compare target ONTAP versions → Fix and acknowledge blockers and review warnings → Accept the license agreement and start the update

**Validate update results:** Complete the cluster update → Wait for *AutoSupport* processing to refresh service data → Open *Health* > *Software updates* → Check the *History* tab for update status
