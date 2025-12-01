# [HaloITSM]

| Detail       | Description                         |
|--------------|-------------------------------------|
| **Availability** | Generally Available  |
| **Plan**         | Starter, Pro, Enterprise            |
| **Permission**   | Owner, Admin                        |


---

:::(Warning) (Note on third‑party tools) 
We aim to provide accurate and helpful details about third‑party tools, but we can’t guarantee that this information is always complete or up to date. If you notice any discrepancies, feel free to share them in the feedback section below. For the most reliable information, please always refer to the third‑party tool’s official documentation. 
:::

HaloITSM is a fully integrated Enterprise Service Management platform designed to simplify service delivery, automate processes, and improve visibility across enterprise operations.
HaloITSM can consume Lansweeper data in two main ways:

1. via Halo Asset Discovery (Lansweeper Site), and
2. via the Lansweeper Integration for direct connectivity to an existing Lansweeper environment (typically on-prem or self-hosted). 

Integrating HaloITSM with Lansweeper allows organisations to synchronise discovered assets directly into HaloITSM, enriching the CMDB and ensuring teams always work with up-to-date device and software information. This supports better incident management, streamlined change processes, and stronger compliance controls.

## Use cases

This integration enables:
- 🔍 Automated IT asset discovery in HaloITSM -> Sync hardware, software, and network inventory directly from Lansweeper.

- 🔄 Continuous CMDB enrichment -> Keep configuration item data accurate without manual updates.

- 🧩 Improved incident and request handling -> Technicians can immediately view linked device details when working on tickets.

- 📊 Enhanced reporting and compliance -> Use Lansweeper-powered asset details to improve audits, software compliance, and lifecycle management.

- ⚙️ Cross-platform automation -> Trigger HaloITSM workflows based on changes detected in Lansweeper (e.g., new device discovered, software changes).

##  Prerequisites

- A complete Lansweeper On-Premise Installation (for the Lansweeper Integration)
- An active Lansweeper Site with API access (for the Halo Asset Discovery Integration)
- A HaloITSM environment where you have Admin permissions
- An On-Premise Halo Integrator to facilitate the daily sync of data(for the Lansweeper Integration)

## Integrate HaloITSM with Lansweeper

**Option 1 – Halo Asset Discovery (Lansweeper Site)** - Recommended for most users

1. Enable Halo Asset Discovery in Configuration > Integrations > CMDB.
2. Enter your Halo Asset Discovery connection details (tenant, key, or endpoint as provided in the guide).
3. Configure your field mappings, choosing which Lansweeper fields map to Halo asset fields (e.g., serial number, device name, OS).
4. Add any optional filters such as limiting import to certain asset types or sites.
5. Run your initial import and verify assets appear correctly in the CMDB.
6. Enable ongoing sync to keep asset information up to date.
7. This option uses a fully managed, cloud-based version of Lansweeper hosted by Halo and requires no on-prem setup.

**Option 2 – Lansweeper Integration (Existing Environment)** - Recommended for users using a standalone Lansweeper On-Premise Installation.

1. Enable the Lansweeper Integration under Configuration > Integrations > CMDB.
2. Enter your credentials for read-only access to the database that your existing Lansweeper environment is installed on.
3. Configure mappings to match Lansweeper device types and attributes with Halo asset types and fields.
4. Apply optional filters and choose whether Halo should create, update, or create & update assets based on discovered data.
5. Run your initial import and verify asset records.
6. Configure scheduled synchronisation to keep the CMDB current via the Halo Integrator.

## Next steps - turning data into information

After connecting HaloITSM and Lansweeper, consider:

- Setting up automated workflows that trigger when assets change
- Creating visual dashboards in HaloITSM showing asset health, software usage, or lifecycle stages
- Linking Incidents, Problems, and Changes to discovered CIs for full traceability
- Configuring user permissions for teams managing assets or working with CMDB modules

## More information

- [HaloITSM Guides Page](https://usehalo.com/haloitsm/guides/)
- [Lansweeper integration guide](https://usehalo.com/haloitsm/guides/1073)
- [Halo Integrator Guide](https://usehalo.com/haloitsm/guides/1766)
- [Halo Asset Discovery integration guide](https://usehalo.com/haloitsm/guides/1783)
- [Best practices for CMDB (Service Automation Framework)](https://haloitsm.com/wp-content/uploads/2024/01/Service-Automation-Framework-9.pdf)
