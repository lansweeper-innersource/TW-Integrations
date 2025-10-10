:::(Warning) (Note on third‑party tools) 
We aim to provide accurate and helpful details about third‑party tools, but we can’t guarantee that this information is always complete or up to date. If you notice any discrepancies, feel free to share them in the feedback section below. For the most reliable information, please always refer to the third‑party tool’s official documentation.
:::

Integrate [Devicie](https://www.devicie.com) with Lansweeper to modernize your device management capabilities and gain deeper visibility into endpoint health and compliance across your organization.  

**Devicie** is an endpoint management platform designed to help IT teams securely deploy, control, and maintain their device fleets remotely and at scale. Integrating Devicie with **Lansweeper** enhances your ability to identify and address compliance and usage anomalies that might otherwise go unnoticed.

---

## Use cases

- Gain unified visibility into device health, compliance, and configuration status.  
- Identify unmanaged or unencrypted devices posing security risks.  
- Automate application patching, encryption, and endpoint hardening.  
- Leverage Microsoft licenses more effectively by configuring Intune and Defender for Endpoint through Devicie.  
- Identify and mitigate risky Windows services and features to improve compliance with CIS benchmarks.  
- Maintain an ongoing audit of devices, local admin accounts, and patch status directly from Lansweeper.

## Prerequisites

Before integrating, ensure you have:

- An active **Lansweeper Site**.  
- Access to the **Lansweeper Marketplace**.  

## Integrate Devicie with Lansweeper

1. In your Lansweeper Site, navigate to **Marketplace > Integrations** and select **Devicie Endpoint Health** from the list.  
2. Select **Add Dashboard**.  
3. Fill in your contact details in the request form to confirm your consent to be contacted by **Devicie** (this is required to activate your dashboard).  
4. Click **Submit** again to finalize setup.  

The **Devicie Endpoint Health** dashboard is added to your Lansweeper Site. To view it, go to **Dashboard > Devicie Endpoint Health**.


## Use the Devicie Dashboard

The Devicie integration adds a custom dashboard to your Lansweeper Site that provides a range of reports offering deep insight into your device health and security posture.

### **Available Reports**

- **Total Devices:** Displays the total number of devices discovered in your environment.  
- **Unmanaged Devices:** Identifies unmanaged devices that increase security risk; Devicie supports onboarding macOS and mobile devices.  
- **Unencrypted Devices:** Highlights unencrypted devices vulnerable to data breaches.  
- **App Audit:** Lists unpatched or vulnerable applications.  
- **Microsoft Licenses:** Helps configure Intune and Defender for Endpoint to optimize Microsoft license use.  
- **Local Administrator Accounts:** Lists local admin accounts to mitigate privilege risks.  
- **Local Administrator Accounts by Name:** Provides detailed visibility into admin accounts.  
- **Risky Windows Services:** Identifies and disables unnecessary services following CIS standards.  
- **Risky Windows Features:** Flags and removes unneeded Windows features to reduce attack surface.  
- **Unencrypted Devices by OS:** Breaks down unencrypted devices by operating system.  
- **Unencrypted Devices by Name:** Provides per-device details for unencrypted endpoints.  
- **Windows Patch Tuesday Audit:** Displays patch compliance status for operating systems.  

For additional report customization or insights, visit the official [Devicie website](https://www.devicie.com).

## Remove Devicie Endpoint Health from Lansweeper

1. Go to **Marketplace > Integrations > Devicie Endpoint Health**.  
2. Select **Remove Dashboard**.  

## More information

- [Devicie Official Documentation](https://www.devicie.com)
- [Lansweeper API Reference](https://developer.lansweeper.com/)