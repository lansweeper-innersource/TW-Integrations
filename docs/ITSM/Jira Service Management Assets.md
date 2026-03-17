The Lansweeper App for Jira Service Management Assets enables seamless and efficient asset management. This integration fetches Lansweeper Assets and synchronizes them directly to Jira Service Management Assets, ensuring that your asset inventory is consolidated and up-to-date. You can schedule syncs at specific intervals based on your preferences, ensuring that your JSM Assets always reflect the latest information from Lansweeper. Advanced configurations let you filter asset types and fields, providing a tailored sync experience that aligns with your needs.

## Features

### Automated sync of Lansweeper Assets with Jira Assets

- Sync Assets from Lansweeper and add them to Jira Assets.
- Configure and control the syncing interval.
- Create new Jira Assets if they don't already exist or update existing assets.

### Filter asset types

- View the list of all existing asset types for the configured Lansweeper Site.
- Turn on or off syncs for specific asset types.
- Find specific asset types through a search function.

### Assets field configuration

- Configure Asset fields that need to be synced from Lansweeper to Jira Assets.
- Add up to 30 fields, including existing fields.

### Sync statistics

- View the status of the sync process, including the start time, end time, and status.

## Prerequisites

- A properly configured Jira Cloud instance.
- A Standard, Premium or Enterprise plan for the Service Collection and Jira Service Management cloud. See [Change your plan](https://support.atlassian.com/jira-cloud-administration/docs/explore-jira-cloud-plans/#Change-your-plan) for more information.
- A Pro or Enterprise plan for Lansweeper. See [Pricing & Plans](https://www.lansweeper.com/pricing/) for more information.
- A Jira admin user.

### Compatibility

| Component | Version/Details |
|---|---|
| Supported Browsers | Google Chrome |
| Lansweeper REST API Version | v2 |
| Development Platform | Atlassian Forge |
| Jira REST API Version | v3 |
| Forge CLI Version | v10.6.1 |
| Supported Lansweeper Platform | Lansweeper Cloud |
| App Hosting Type | Cloud |
| Supported Products | Jira Service Management (Premium or Enterprise plan) |

## Install the Lansweeper app

1. In your Jira Service Management account, go to **Apps > Explore more apps**.
2. In the search bar, enter **Lansweeper App for Jira Service Management Assets**.
3. Select **Lansweeper App for Jira Service Management Assets**, then select **Get it now**.
4. The installation process begins. A message appears once the successful installation is completed.


:::(Info)
If you don't get the success notification for the installation, create an Atlassian support ticket, explain the issue, and attach a screenshot of the message.
:::

## Configure the app

### Prepare credentials

Ensure you have the following credentials available before you begin:

- Lansweeper API URL
- [Lansweeper PAT API Client](https://developer.lansweeper.com/docs/data-api/get-started/quickstart/#personal-access-token-pat)
- Atlassian User Email Address (with Jira Admin rights)
- [Atlassian API Token](https://id.atlassian.com/manage-profile/security/api-tokens)

### Verify your plan

Ensure that the Premium or Enterprise plan is enabled for the Jira Service Management cloud. If not, [change your plan](https://support.atlassian.com/jira-cloud-administration/docs/explore-jira-cloud-plans/#Change-your-plan).

### Connect Lansweeper and Atlassian

1. In your Jira Service Management account, go to **Apps > Manage your apps**.
2. From the left pane, select **Lansweeper App for Jira Service Management Assets Configuration**.
3. Select **Allow access** to allow the Lansweeper app to access Atlassian products on your behalf.
4. Review what the Lansweeper app has access to, then select **Accept**.
5. Select the **Connections** tab.
6. Enter the Lansweeper API URL and Lansweeper Personal Access Token under the Lansweeper Credentials section.

### Create an object schema

We recommend [creating a new Object Schema](https://support.atlassian.com/jira-service-management-cloud/docs/create-an-object-schema/) for your Lansweeper app.

1. Open the JSM Assets menu in another browser tab.
2. Select **Create Schema**.
3. Select **Create a blank schema**.
4. Fill in the schema information fields.
5. Select **Create schema**.
6. In the Object Schema view, select **Schema configuration** on the left.
7. Select **Roles** tab
8. Add the Lansweeper app to the Object Schema Manager role.

### Configure the import

1. In the Object Schema view, select **Schema configuration** on the left.
2. Select the **Import** tab, then select **Create import**.
3. Select **External Import** as your import type, then select **Next**.
4. Fill out the fields for your import configuration.
5. Select **Create import**.
6. Select the three dots icon, then select **Generate new token**.
7. Copy the Assets Import Token by selecting the copy icon.

### Complete the configuration

1. Switch to the app configuration tab.
2. In the Atlassian Credentials section, enter the Jira Admin Email Address and Atlassian API Token.
3. Select **Load Object Schema** to load the list of Object Schemas, then select **Continue** to view the list.
4. Select the blank schema that you created in the previous steps (for example, **Lansweeper Assets**).
5. Select the next field and paste the **Assets Import Token** that you generated for your import settings.
6. In the Scheduler Configuration section, select the interval you prefer. Available options are hourly, daily, and weekly.
7. Select **Validate and Save** to validate and save the configuration.

:::(Info)
Once the configurations are saved successfully, all fields on the configuration page will be disabled and can only be updated after you reset the configuration.
:::

## Filter asset types

After completing the connection configurations, you can enable or disable asset type synchronization by navigating to the **Asset Types** tab.

:::(Info)
We recommend enabling only the necessary asset types for your JSM use cases. Keeping the JSM Assets environment focused with usable data is important for the success of your ITSM/ESM implementation.
:::

Use the search bar to find specific assets.

## Configure asset fields

To configure asset fields, go to **Apps > Manage your apps > Lansweeper App for Jira Service Management Assets Configuration > Asset Fields**.

From there, you can view the list of available asset fields. Some fields are required and therefore not configurable.

### Edit or remove fields

You can remove some fields by deleting the **Jira Asset Field Name** and its corresponding **Lansweeper Field Name**. You can also edit the **Jira Asset Field Name**. Select **Validate and Save** to save your configuration.

### Add new asset fields

1. Find the Lansweeper Field name you desire from the list of available [asset types](https://developer.lansweeper.com/docs/data-api/reference/types).
2. Select the field name to copy its full name to your clipboard.
3. In the **Asset Fields** table, scroll to an empty row and paste your copied field name in the **Lansweeper Field Name** column.
4. Enter a name in the **Jira Asset Field Name** column.
5. Select **Validate and Save**. A success message appears if the configuration has been successful.

To restore default settings, select **Restore Default**.

## Custom asset fields

In addition to the standard Lansweeper Asset Fields, you can view the list of Custom Asset Fields on the related tab.

1. Enable or disable the fields to decide which ones you want to import.
2. If you have many custom fields, use the search function to find the one you would like to configure.

## Software and vulnerabilities

Under the Software/Vulnerabilities menu, you can enable two options:

### Software import

Enable the Software Import to import the list of software and their versions into JSM Assets from your Lansweeper environment. Once the data is imported, you will also find links to the Lansweeper software records to investigate which assets have the related software installed.

### Vulnerabilities import

Enable the Vulnerabilities Import to import the list of vulnerabilities and their relations to the Lansweeper Assets. Once the data is imported, you will also find links to the Lansweeper vulnerability records to investigate more.

## Data import

There are two ways to import data from Lansweeper: manual import and automated scheduled import.

### Run full sync

After the successful configuration, the **Run Full Sync** button becomes enabled on the **Connection** tab. This button updates the Object schema and all Assets.

:::(Info)
You must run a full sync if this is your first time using the app or you changed the configuration in any of the following settings:

- Asset Types
- Asset Fields
- Custom Asset Fields
- Software/Vulnerability
:::

1. Select the **Run Full Sync** button to start the full data synchronization process.
2. A success message will appear when the activity starts on the bottom left of the page.

### Scheduled import

The scheduled import runs at the selected interval and performs full data synchronization.

## Check sync statistics

Go to **Apps > Manage your apps > Lansweeper App for Jira Service Management Assets Configuration > Statistics**.

You can see the previous five sync attempts from here, including their start time, end time, and status.

## View and manage assets

### View assets

1. In your Jira Service Management account, select **Hardware**. All of the asset types that have been imported from Lansweeper are displayed within the Hardware section.
2. Select an asset type from the list. The asset type window is displayed, including a list of all the assets of that type.
3. Select an asset from the list for more information, including the asset name, key, host site, and more. Select the Lansweeper Asset URL link to view the asset on your Lansweeper Site. See [configure asset fields](/classic/docs/license-issue-for-cloud#configure-asset-fields) to edit these fields.
4. In the **Linked issues** section, view any Jira issues that have been created that are related to the asset.

### View linked objects

The Lansweeper app allows you to easily view which objects are linked to each other.

1. Go to **Assets > Hardware** and select the asset type you desire from the list, then select the specific asset from that type.
2. In the Linked objects section, you can view the outbound and inbound references and their relation types.

Select the object link to be taken to that asset's page.

### View object graph

The object graph provides a visual representation of your linked objects.

1. Go to **Assets > Hardware** and select the asset type you desire from the list, then select the specific asset from that type.
2. In the Linked objects section, select **Object graph**.

Select the object link in the right pane to be taken to that asset's object graph.

## Uninstall the app

1. In your Jira Service Management account, go to **Apps > Manage your apps**.
2. Select **Lansweeper App for Jira Service Management Assets > Uninstall**.
3. In the pop-up, select **Uninstall app**.

## Troubleshooting

### General issues

If an error or issue arises, check the application logs to determine what has occurred.

1. Log into [Atlassian Admin](https://admin.atlassian.com/) as a system administrator.
2. Select **Products > Sites and products**.
3. Select **Connected Apps**.
4. Select the three dots, then select **Download logs**.

### Unable to install or activate the app

If an error occurs while attempting to install or activate the Lansweeper app on Jira Cloud, review and follow the steps on [Installing Marketplace apps](https://confluence.atlassian.com/upm/installing-marketplace-apps-273875715.html).

### Permission errors

If the permissions are not correctly set after you install the Lansweeper app, attempt the following fixes:

**Option 1: Reinstall the app**

Uninstall the app, then reinstall and reconfigure the app.

**Option 2: Revoke access**

1. Go to [Atlassian Admin](http://admin.atlassian.com/). Select your organization if you have more than one.
2. Select the site's name and URL to open the Admin for that site.
3. Select **Products**, then select the site from the left-hand side.
4. Select **Connected apps** from the Site Settings menu.
5. Select **Manage authorization** for the app.
6. Select **Revoke access**.
7. Reload the configuration page.

If issues persist, contact [Lansweeper Support](https://www.lansweeper.com/contact-support/).

## Known behaviours

- Any configuration parameter changes made after the sync process has started will not affect the current sync process and will be reflected in the next sync.
- In case of deletion of assets from the Lansweeper side, the deleted assets may remain in JSM Assets.
- If you reset the configuration page while a syncing process is currently running, the syncing process may fail.
- If an unexpected error occurred during the sync process, the status of the process will remain in the in-progress state and you may need to wait for 24 hours after which the sync progress is reset automatically. You can also reset the configuration to restart the sync process.
- At max 100 object schemas will be shown in the "Select Object Schema" select button on the App configuration page.
- If any failure occurs at some point during the asset ingestion process, the app will retry the failed function a maximum of 4 times. The app will mark the sync process as failed if the error persists.
- Due to a limitation from the Atlassian Jira side, you may be unable to access the user-side logs.
- In Asset Fields Mapping, a new field is created into the current object schema whenever you change an existing Jira asset field name or add a new Jira assets field. The mapping changes will be reflected in the next sync cycle. The currently running sync process may get affected by new mapping changes as the current checkpoint will be removed after the mapping changes are validated and saved successfully.
- You need to refresh the page to see new asset types in the Asset Types tab.
- If any asset is manually added to JSM Assets, it will remain as it is and will not be affected by the sync unless it has the same asset key as the Lansweeper Asset.
- If any asset is deleted from JSM Assets, it will get recreated if it comes under the next scheduled sync from Lansweeper, which brings the updated assets after the last sync.
- If any attribute of an LS Asset is updated in JSM Assets, then it would get overwritten if the same asset with the updated field comes under the next scheduled sync from Lansweeper, which brings the updated assets after the last sync.

:::(Info)
Lansweeper's APIs allow you to develop apps that seamlessly integrate our market-leading IT discovery and inventory platform. Find everything you need to get started in our [Developer Portal](https://developer.lansweeper.com/?utm_source=referral&utm_medium=website&utm_campaign=ls-dev_portal-global-q4-2024&utm_content=kb_article-sentence_cta%20or%20Developer%20Portal).
:::
