:::(Warning) (Note on third‑party tools)  
We aim to provide accurate and helpful details about third‑party tools, but we can’t guarantee that this information is always complete or up to date. For the most reliable information, please always refer to the third‑party tool’s official documentation.  
:::

The ConnectWise integration automatically synchronizes assets from Lansweeper into ConnectWise PSA as configurations. It creates new configurations and updates existing ones by managing reference data, applying matching logic, and performing batched operations for optimal performance.

The integration also syncs metadata and relationship details, such as agreements and tickets, and updates Lansweeper assets with this contextual information to keep data consistent across both systems

## Use cases

This integration allows you to:  

- Enable seamless integration with the ConnectWise API to synchronize configurations, agreements, SLAs, and tickets.
- Automatically sync Lansweeper’s detailed hardware, software, and network discovery data into ConnectWise PSA, eliminating manual data entry and mismatched records.
- Give technicians instant, context‑rich visibility into device specs, OS details, users, and warranties directly within PSA tickets, speeding up troubleshooting and improving first‑line resolution rates.
- Trigger proactive service automation in ConnectWise PSA by turning Lansweeper alerts, such as expired warranties or missing antivirus protection, into automated tickets or workflows.
- Link Lansweeper‑discovered assets to PSA contracts for accurate asset‑based billing, ensuring complete and transparent invoicing.
- Simplify client onboarding by importing full IT inventories from Lansweeper into PSA in minutes, enabling immediate insights and reduced setup time.

## Prerequisites

Before you start, ensure you have:  
- An active **Lansweeper Site** with integration access.
- A role with permission to **Enable integrations** in Lansweeper.  
- Access to your **ConnectWise** environment with sufficient privileges.  

## Integrate ConnectWise with Lansweeper

### Create configuration custom fields in ConnectWise  
1. In ConnectWise, navigate to **System > Setup Tables** and search for **Custom Fields**.  
2. In **Pod Description**, search for **Configuration Details**.  
3. Create the following custom fields (you can choose the display names):  

   | Field Name | Type | Description |
   |-------------|------|-------------|
   | `ls_asset_id` | Text | Stores Lansweeper asset ID. |
   | `ls_asset_url` | Text | Stores Lansweeper asset URL. |
   | `ls_asset_location` | Text | Stores Lansweeper asset location. |
   | `ls_software` | Textarea | Stores installed software from Lansweeper. |

4. Make note of the **field IDs**, as they’ll be required in the Lansweeper integration configuration.

### Create an API Key in ConnectWise  
1. In ConnectWise, go to **My Account > API Keys**.  
2. Create a new API key and copy both the **Public Key** and **Private Key**.  
3. These keys will authenticate the Lansweeper–ConnectWise connection.  

### Enable and configure the integration in Lansweeper  
1. In Lansweeper, navigate to **Marketplace > ConnectWise**.  
2. Select **Enable** on the integration detail page. If the button is disabled, request **Enable integrations** permission from your site owner.
3. In the configuration wizard, provide the required details:  

   - **ConnectWise PSA Site**: The URL of your ConnectWise PSA environment, found in **System > My Company > Site URL for Manage**.  
   - **ConnectWise Company ID**: The company identifier, found in **System > My Company > Customer Portal URL Override**. For example, if the URL is `staging.connectwisedev.com/lansweeper_f`, the company ID is `lansweeper_f`.  
   - **ConnectWise Public/Private Keys**: The API keys you generated in ConnectWise.
   - **software_cf_id**: The custom field ID of `ls_software`.  
   - **assetKey_cf_id**: The custom field ID of `ls_asset_id`.  
   - **assetUrl_cf_id**: The custom field ID of `ls_asset_url`.  
   - **assetLocation_cf_id**: The custom field ID of `ls_asset_location`.

5. Set the **Schedule flow trigger** to define how often data should synchronize.  
6. Select **Next**, then choose which **ConnectWise company** the configurations will belong to.   

When successful, the integration runs automatically based on your configured schedule.  

## Next steps

After successful setup:  

- Confirm that Lansweeper assets appear as **Configurations** in ConnectWise PSA.
- Review automatic custom fields created in Lansweeper for **tickets** and **SLA** information.
- Adjust sync frequency or data‑mapping settings as needed.
- Create additional automated workflows using Lansweeper’s Flow Builder [ConnectWise Connector](https://community.lansweeper.com/t5/connectors/connectwise-connector/ta-p/85880) to act on asset events.
- If needed, disable the Connectise integration by navigating to **Marketplace > ConnectWise** and selecting **Disable**.

## More information

- [ConnectWise PSA official documentation](https://university.connectwise.com/)
- [ConnectWise official site](https://www.connectwise.com/)
