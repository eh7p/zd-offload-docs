---
title: Microsoft Sharepoint Guide
layout: default
parent: Bring Your Own Storage (Hybrid)
---
# Microsoft Sharepoint
{: .no_toc }

1. TOC
{:toc}

## Microsoft Sharepoint Connection Setup

After sign-up, select the Hybrid option and then the Microsoft Sharepoint provider.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.png" alt="Screenshot of the Hybrid provider selection">
</picture>

You'll be prompted to sign-in to your Microsoft Account and asked for permissions to read/write to your Sharepoint drive.

Next provide your:
- Sharepoint Drive ID

_For setting these up, see [Finding Your Sharepoint Drive ID](#finding-your-sharepoint-drive-id) below_
{: .fs-3 .text-grey-dk-000 }

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/connection-details.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/connection-details.png" alt="Screenshot of the Sharepoint provider hybrid setup">
</picture>

'Save & Test' will attempt to write and read a file on the storage provider. Once tested, you will be asked to confirm the connection parameters.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/confirm.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/confirm.png" alt="Screenshot of the Sharepoint provider hybrid setup confirmation">
</picture>

The solution is now connected to your Microsoft Sharepoint.

## Finding Your Sharepoint Drive ID

Navigate to the Microsoft Graph Explorer <a href="https://developer.microsoft.com/en-us/graph/graph-explorer">https://developer.microsoft.com/en-us/graph/graph-explorer</a> and sign into your Microsoft account, the tenant should show your organisation (not 'Tenant Sample')

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/graph-logged-in.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/graph-logged-in.png" alt="Screenshot of the Microsoft Graph Explorer signed in as a user">
</picture>

Run a query for `https://graph.microsoft.com/v1.0/sites/{sharepoint domain}:/sites/{site name}`

For instance if your Sharepoint site lives at `https://eh7p.sharepoint.com/sites/ZendeskOffload/`, your query would be `https://graph.microsoft.com/v1.0/sites/eh7p.sharepoint.com:/sites/ZendeskOffload`

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/graph-site.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/graph-site.png" alt="Screenshot of the Microsoft Graph Explorer showing a sharepoint site details">
</picture>

Run a query for `https://graph.microsoft.com/v1.0/sites/{site id}/drives`

For instance if the ID from the previous query was `eh7p.sharepoint.com,70b4d76a-2caf-4b70-a054..................`, your query would be `https://graph.microsoft.com/v1.0/sites/eh7p.sharepoint.com,70b4d76a-2caf-4b70-a054................../drives`

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/graph-drive.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/graph-drive.png" alt="Screenshot of the Microsoft Graph Explorer showing a sharepoint drive details">
</picture>

The ID shown here is the Drive ID, in this case `b!ate0cK8scEug.......................`.

### Graph Explorer Permissions

While using the Graph Explorer you may need to enable the `Sites.Read.All` permission.

## Testing

To test the solution, once the solution and hybrid connection is setup, navigate to the tickets view on the dashboard and select a ticket to extract the attachments for.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.png" alt="Screenshot of the Zendesk Storage Offload dashboard showing a ticket which has not yet been extracted">
</picture>

Now extract the ticket, the files will be shown within the Microsoft Sharepoint Documents

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/extracted-attachments.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/sharepoint-storage/extracted-attachments.png" alt="Screenshot of the Microsoft Sharepoint Bucket showing the extracted files">
</picture>


If you require an alternative file naming schema, please [get in touch]({% link docs/contact-us.md %})!