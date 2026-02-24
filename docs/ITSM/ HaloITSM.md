<!--# [HaloITSM]-->

:::(Warning) (Note on third‑party tools) 
We aim to provide accurate and helpful details about third‑party tools, but we can’t guarantee that this information is always complete or up to date. For the most reliable information, please always refer to the third‑party tool’s official documentation. 
:::

HaloITSM is a fully integrated Enterprise Service Management platform designed to simplify service delivery, automate processes, and improve visibility across enterprise operations.

HaloITSM can consume Lansweeper data using either:

- Halo Asset Discovery for Lansweeper Sites
- Halo's Lansweeper Integration for direct connectivity to an existing Lansweeper On-Premises or self-hosted environment

Integrating HaloITSM with Lansweeper allows organizations to synchronize discovered assets directly into HaloITSM, enriching the CMDB and ensuring teams continuously work with up-to-date device and software information. This supports better incident management, streamlined change processes, and stronger compliance controls.

## Use cases

- **Automated IT asset discovery in HaloITSM**: Sync hardware, software, and network inventory directly from Lansweeper.
- **Continuous CMDB enrichment**: Keep configuration item data accurate without manual updates.
- **Improved incident and request handling**:  Allow technicians to immediately view linked device details when working on tickets.
- **Enhanced reporting and compliance**: Use Lansweeper-powered asset details to improve audits, software compliance, and lifecycle management.
- **Cross-platform automation**: Trigger HaloITSM workflows based on changes detected in Lansweeper (e.g., new device discovered, software changes).

##  Prerequisites

**Halo Asset Discovery for Lansweeper Sites**:
- A HaloITSM environment where you have Admin permissions
- An active Lansweeper Site with API access 

**Halow's Lansweeper Integration for Lansweeper On-Premises**:
- A HaloITSM environment where you have Admin permissions
- A complete, standalone Lansweeper On-Premises installation
- An on-premises Halo Integrator to facilitate the daily sync of data

## Integrate Halo Asset Discovery with Lansweeper Sites

Halo Asset Discovery is recommended for users with a Lansweeper Site. This option uses a fully managed, cloud-based version of Lansweeper hosted by Halo and requires no on-premises setup.

1. In your HaloITSM environment, go to **Configuration > Integrations > CMDB** and enable **Halo Asset Discovery**.
2. Enter your connection details (tenant, key, and endpoint) as provided in the Halo setup guide.
3. Configure your field mappings and choose which Lansweeper fields map to Halo asset fields (for example, serial number, device name, or operating system).
4. (Optional) Add filters to limit imports to specific asset types or sites.
5. Run the initial import and verify that assets appear correctly in the CMDB.
6. Enable ongoing synchronization to keep asset information up to date.

## Integrate Halo's Lansweeper Integration with Lansweeper On-Premises

Halow's Lansweeper Integration is recommended only for users with a standalone **Lansweeper On‑Premises** installation.

1. In your HaloITSM environment, go to **Configuration > Integrations > CMDB** and enable **Lansweeper Integration**.
2. Enter your credentials for read-only access to the database where your Lansweeper environment is installed.
3. Configure mappings between Lansweeper device types and attributes and Halo asset types and fields.
4. (Optional) Apply filters and choose whether Halo should **create**, **update**, or **create and update** assets based on discovered data.
5. Run the initial import and verify the imported asset records.
6. Configure scheduled synchronization to keep the CMDB current through the Halo Integrator.

## Next steps: Turn data into information

After you connect HaloITSM and Lansweeper, you can:

- Set up automated workflows that trigger when asset data changes.
- Create visual dashboards in HaloITSM to track asset health, software usage, and lifecycle stages.
- Link Incidents, Problems, and Changes to discovered configuration items (CIs) for full traceability.
- Configure user permissions for teams that manage assets or work with CMDB modules.

## More information

- [HaloITSM guides](https://usehalo.com/haloitsm/guides/)
- [Lansweeper Integration guide](https://usehalo.com/haloitsm/guides/1073)
- [Halo Integrator guide](https://usehalo.com/haloitsm/guides/1766)
- [Halo Asset Discovery integration guide](https://usehalo.com/haloitsm/guides/1783)
- [Best practices for CMDB (Service Automation Framework)](https://haloitsm.com/wp-content/uploads/2024/01/Service-Automation-Framework-9.pdf)
