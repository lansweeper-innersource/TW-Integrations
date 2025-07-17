# Integrate Licenseware with Lansweeper

The integration of Licenseware with Lansweeper offers a comprehensive solution that streamlines the process of gathering crucial license information. This integration removes the need to use manual methods or costly consultancy services to manage software assets. Instead, you can swiftly access granular data about your software assets, empowering you to make informed licensing decisions quickly and accurately.

This integration also allows you to effortlessly identify unsupported versions and potential security risks, ensuring proactive risk mitigation strategies. The Licenseware and Lansweeper integration supports effective software asset management, paving the way to enhanced compliance, cost optimization, and operational efficiency.

Additionally, the integration can support the following Licenseware apps: Microsoft, RedHat, and Oracle.

## Use cases

The Licenseware integration supports the following use cases:

- Providing visibility into Java licensing compliance following Oracle’s pricing change
- Supporting MSPs with effective software asset management
- Managing Microsoft product deployments and licensing requirements

## Create an API Connection

To integrate Licenseware and Lansweeper, we recommend creating an API connection, which allows Lansweeper data to automatically sync with Licenseware.

To create the API connection:

1. In your Lansweeper Site, go to **Settings > Developer tools > All Applications**.  
2. Select **Add new application**.  
3. Select **Personal application > Continue**.  
4. Enter a name for the application, such as “Licenseware API.”  
5. In the Integration dropdown, select **Licenseware**.  
6. Select **Add application**.  
7. Select your application from the list.  
8. Under **Sites authorization**, select **Authorize**.  
9. Select when you want your access token to expire.  
10. Select which of your sites you want to grant Licenseware access.  
11. Copy the Application identity code.  
12. Navigate to Licenseware and select the target project.  
13. Select **Integrations**.  
14. Select **Lansweeper Cloud > Configure**.  
15. Paste your application code into the application identity code field.  
16. Select **Update** to establish a connection between Lansweeper and Licenseware.  
17. Toggle the following options if you want the data to sync:
    - Hardware and visualization data  
    - Installed Microsoft software  
    - Java installations and device user information  

Once the connection is complete, Lansweeper’s data will automatically sync to Licenseware.

### Add Lansweeper data manually

Alternatively, you can manually add Lansweeper data to Licenseware using custom reports, if you’d prefer not to connect the solutions via API.

To manually add Lansweeper data, follow the instructions on **How to get and use Lansweeper data for Microsoft Deployment Manager**. Although the instructions are specifically for the Microsoft Deployment Manager app, the same process can be applied to the other Licenseware apps.

## Leverage the Software Inventory Manager (SIM) app

The SIM app, developed by Licenseware and powered by Lansweeper’s discovery technology, is designed to help you effectively manage your software assets. By providing a complete view of your software environment, SIM allows you to address key aspects of Software Asset Management (SAM) like compliance, cost efficiency, and risk mitigation.

SIM uses advanced recognition to identify all installed software and provides actionable insights to streamline decision-making.

### Key benefits and use cases

- **Compliance and risk management:**  
  SIM provides real-time insights into software assets, helping you identify areas at risk of non-compliance. This reduces the chance of costly audit penalties by flagging software requiring licensing or monitoring potential instances of shadow IT.

- **Cost efficiency:**  
  With a focus on cost optimization, SIM helps rationalize software portfolios by highlighting redundant or underused installations, identifying budget-saving opportunities, and supporting more informed decisions on renewals, standardization, or discontinuation.

- **Visibility and control:**  
  SIM enhances asset visibility by creating a complete, up-to-date inventory that’s easy to track, making it simpler for IT teams to understand software usage patterns, manage software sprawl, and maintain control over licensing complexities.

To learn more about Licenseware and the SIM app, check out [**Lansweeper + Licenseware for Software Asset Management**](https://www.lansweeper.com/product/integrations/financial-strategic-planning/licenseware/).


:::note

Lansweeper’s APIs allow you to develop apps that seamlessly integrate our market-leading IT discovery and inventory platform. Find everything you need to get started in our **Developer Portal**.

:::