<!--
🎨 Ownership key (for internal reference — can be removed or ignored by contributors)
> 🔵 Blue = Integration provider-owned
> 🟠 Orange = Lansweeper-owned
-->

| Detail           | Description                             |
|------------------|-----------------------------------------|
| **Availability** | Generally Available                     |
| **Plan**         | Pro, Enterprise                         |
| **Permission**   | Owner, Admin                            |

---

:::(Warning) (Note on third‑party tools) We aim to provide accurate and helpful details about third‑party tools, but we can’t guarantee that this information is always complete or up to date. If you notice any discrepancies, feel free to share them in the feedback section below. For the most reliable information, please always refer to the third‑party tool’s official documentation. :::

[Licenseware](https://www.licenseware.io/) is a third-party solution that helps businesses manage licensing, assess compliance, and reduce software spend through modular, automation-driven apps.

Integrating **Licenseware** with **Lansweeper** allows you to automate the flow of device and software inventory data from Lansweeper to Licenseware applications, reducing manual work, improving audit readiness, and helping organizations make more informed licensing decisions.

## Use Cases

- Provide visibility into **Java licensing compliance**, following Oracle’s licensing model changes.
- Manage Microsoft product deployments and licensing requirements. 
- Help **MSPs** manage clients’ IT environments more holistically and cost-effectively
- Support specialist apps (like **Microsoft**, **RedHat**, and **Oracle**) within Licenseware

## Prerequisites

- A Lansweeper Site where you're an admin or owner
- A valid Licenseware account
- Internet access between the two platforms (no firewalls blocking integration endpoints)

## Integrate Licenseware with Lansweeper

### Option 1 – Connect via API (Recommended)

In your Lansweeper Site:

1. Go to **Settings > Developer Tools > All Applications**.
2. Select **Add new application**.
3. Select **Personal application > Continue**.
4. Enter a name for the application (e.g., `Licenseware API`).
5. In the **Integration** dropdown, select **Licenseware**.
6. Select **Add application**.
7. From the list of applications, select your new one.
8. Under **Sites Authorization**, select **Authorize**.
9. Choose when you want your access token to expire.
10. Select the site(s) you want to grant Licenseware access to.
11. Copy the **Application Identity Code**.

In Licenseware:

12. Navigate to your **target project**.
13. Go to **Integrations**.
14. Select **Lansweeper Cloud > Configure**.
15. Paste your Application Identity Code into the designated field.
16. Click **Update** to complete the connection.
17. (Optional) Toggle the data types you’d like to sync:
    - Hardware and virtualization data  
    - Installed Microsoft software  
    - Java installations and device user information

Once complete, Lansweeper data will automatically sync to Licenseware.

---

### Option 2 – Add Lansweeper Data Manually

If you prefer not to connect via API, you can manually add data by exporting custom reports from Lansweeper and uploading them to Licenseware.

We recommend following the steps in the [Lansweeper API or Static](https://help.licenseware.io/mdm-lansweeper-integration) guide.
> Although focused on Microsoft, the process can apply to apps like Oracle and RedHat as well.

---

## Next Steps - Explore the Software Inventory Manager (SIM) App

The **SIM app**, developed by Licenseware and powered by Lansweeper’s discovery technology, helps you manage your software landscape more effectively through automation and rich insights.

By pulling accurate IT asset data from Lansweeper into SIM, you can address core areas of Software Asset Management (SAM), including compliance, cost optimization, and risk reduction.

Learn more:  
[Lansweeper + Licenseware for Software Asset Management](https://www.lansweeper.com/product/integrations/financial-strategic-planning/licenseware/)

## More information

- [Licenseware integrations documentation](https://help.licenseware.io/mdm-lansweeper-integration)
- [Licenseware.io + Lansweeper Integration Provides Visibility into Java Licensing Compliance Following Oracle’s Pricing Change](https://www.lansweeper.com/blog/partners-and-integrations/licenseware-io-lansweeper-integration-provides-visibility-into-java-licensing-compliance-following-oracles-pricing-change/)
- [Licenseware and Lansweeper: A Powerful Combo for Effective Software Asset Management](https://www.lansweeper.com/blog/partners-and-integrations/licenseware-and-lansweeper-a-powerful-combo-for-effective-software-asset-management/)
