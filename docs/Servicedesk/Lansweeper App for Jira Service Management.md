<!--# [Lansweeper App for Jira Service Management]-->

:::(Warning) (Note on third‑party tools)
We aim to provide accurate and helpful details about third‑party tools, but we can't guarantee that this information is always complete or up to date. For the most reliable information, please always refer to the third‑party tool's official documentation.
:::

The Lansweeper App for Jira Service Management (JSM) enriches JSM issues with related Lansweeper assets. The app helps users identify and associate assets with tickets quickly, reducing time spent on manual lookups during incident resolution.

Integrate **Lansweeper App for Jira Service Management** with Lansweeper to automatically surface relevant assets within Jira issues, link related tickets, and give technicians immediate context when working on incidents.

## Use cases

- **Automatic asset matching**: Automatically fetch assets based on IP addresses or MAC addresses found in the issue summary or description.
- **Asset search**: Search Lansweeper assets directly from a Jira issue by IP, MAC address, asset name, user name, manufacturer, or type.
- **Reporter matching**: Match the reporter's email address in Jira with the last logged-in user on a Windows PC in Lansweeper.
- **Issue linking**: Link all Jira issues that share one or more selected assets to the current issue for a consolidated view.
- **Software visibility**: View the list of software installed on a selected asset directly within the Jira issue.

## Prerequisites

- A properly configured Jira Cloud instance with the Lansweeper App installed.
- A Lansweeper instance appropriately configured and populated with assets.
- Admin rights in Jira to configure the app.

### Compatibility

| Component | Version/Details |
|---|---|
| Supported Browsers | Google Chrome, Microsoft Edge, Safari |
| Lansweeper REST API Version | v2 |
| Development Platform | Atlassian Forge |
| Jira REST API Version | v3 |
| Forge CLI Version | v5.2.1 |
| Supported Lansweeper Platform | Lansweeper Sites |
| App Hosting Type | Cloud |
| Supported Products | Jira Software, Jira Service Management, Jira Work Management |

## Install the app

1. Log in to your Atlassian Jira site and go to **Apps > Explore more apps**. Only Jira administrators can access this menu.
2. In the search bar, enter **Lansweeper**.
3. Select **Lansweeper App for Jira**.
4. Select **Get it now > Get it now**. The installation process begins. Once installed, a success message appears in the bottom left.
5. Go to **Apps > Manage your apps**. The **Lansweeper App for Jira** appears in the Apps section on the left.

:::(Info)
If you don't get the success notification for the installation, create an Atlassian support ticket, explain the issue, and attach a screenshot of the message.
:::

### Uninstall the app

1. Go to **Apps > Manage your apps**.
2. Select **Lansweeper App for Jira Service Management**.
3. Select **Uninstall > Uninstall app**.

## Configure the app

### Get a Lansweeper API token

The app requires a Personal Access Token (PAT) from Lansweeper to make API calls from Jira to Lansweeper.

1. [Generate a Personal Access Token (PAT).](https://developer.lansweeper.com/classic/docs/data-api/get-started/quickstart/#personal-access-token-pat) Ensure that you choose the API client type as **PAT (Personal Access Token)**.
2. We recommend setting a long expiration period or no expiration for the token to allow the app to function without interruption.

### Connect Lansweeper and Jira

1. Go to **Apps > Manage your apps**.
2. Select **Lansweeper App for Jira Service Management**.
3. If prompted, select **Allow access** to authorize the app to access Atlassian products on your behalf, then select **Accept**.
4. Enter the API token that you generated in the previous step.
5. Use the **Projects** dropdown to select the projects where you want the app to be active.
6. Select **Validate and Save**. Upon successful validation and authentication, a success message appears.

## Ticket enrichment

Navigate to any Jira issue to see a **Lansweeper** field on the right side of the **Details** tab. Select **View Associated Assets** to open the Asset Details view.

Assets are displayed across three tabs:

**Search Results**

Displays assets fetched from Lansweeper using the search functionality. You can search by IP, MAC address, asset name, user name, manufacturer, type, or All.

Select the assets you need for the ticket using the checkbox.

**Matched**

Displays assets fetched automatically based on IP addresses or MAC addresses found in the issue summary or description. The app also attempts to match the reporter's email address in Jira with the last logged-in user on a Windows PC in Lansweeper.

Select the assets you need for the ticket using the checkbox.

**Selected**

Displays assets that have been selected for the current Jira issue from the Matched and Search Results tabs. For each Jira issue, the asset ID, site ID, and company name are stored per selected asset.

If an asset has software installed, a computer icon appears in the **Info** column. Select the icon to view a list of installed software and their versions.

If an asset has active vulnerabilities, a red bug icon appears in the **Info** column, showing the number of vulnerabilities and their CVE numbers. Select the related link to view vulnerability details.

## Issue linking

In environments where multiple tickets relate to the same asset, the Lansweeper App provides a **Link Related Issue** feature to consolidate related issues automatically.

1. For each ticket, search and select the relevant assets as described in the ticket enrichment section above.
2. Select **Link Related Issue**. This links all Jira issues that share any of the selected assets with the current issue.
3. Refresh the page to see the linked issues.

:::(Info)
Issue linking only applies to issues that do not have the Jira status **Done**. This includes the following statuses: Resolved, Closed, Declined, Canceled, Completed, Failed, Done, Published, Approved, and Rejected.
:::

## Known behavior

- If the API token provided does not have any site selected, an error message is displayed.
- If the linking process is initiated in two issues with the same selected assets simultaneously, duplication may occur for a few linked issues.
- IP addresses and MAC addresses in the issue summary or description must be in plaintext. If they are formatted as links, the related assets may not appear in Asset Details.
- To view newly linked assets, refresh the page after selecting **Link Related Issue**.

## Troubleshooting

### Installation issues

If you don't receive a success notification after installation, create an Atlassian support ticket and attach a screenshot of the message. The installation process is managed by Atlassian.

### Application logs

Check application logs whenever an error or issue occurs. This requires the role of system administrator.

1. Go to [Atlassian Admin](https://admin.atlassian.com/).
2. Select **Products > Sites and products**.
3. Select **Connected Apps**.
4. Select the three dots icon, then select **Download logs**.

### Unable to install or activate the app

If any issue is encountered during installation or activation of the app on Jira Cloud, review and follow the steps on [Installing Marketplace apps](https://confluence.atlassian.com/upm/installing-marketplace-apps-273875715.html).

### Permission errors

To manage users, groups, permissions, and roles in Jira Cloud, see [Manage users, groups, permissions, and roles in Jira Cloud](https://support.atlassian.com/jira-cloud-administration/docs/manage-users-groups-permissions-and-roles-in-jira-cloud/).

### Ticket enrichment UI issues

If any issue occurs while viewing asset details or selecting and deselecting assets, use the refresh button on the right side of the Asset Details page, or hard refresh the browser page.

## More information

- [Lansweeper Developer Portal](https://developer.lansweeper.com/?utm_source=referral&utm_medium=website&utm_campaign=ls-dev_portal-global-q4-2024&utm_content=kb_article-sentence_cta%20or%20Developer%20Portal)
- [Lansweeper Personal Access Token setup](https://developer.lansweeper.com/classic/docs/data-api/get-started/quickstart/#personal-access-token-pat)
- [Installing Marketplace apps](https://confluence.atlassian.com/upm/installing-marketplace-apps-273875715.html)
- [Lansweeper Support](https://www.lansweeper.com/contact-support/)
