---
title: Azure Storage Guide
layout: default
parent: Bring Your Own Storage (Hybrid)
---
# Azure Storage
{: .no_toc }

1. TOC
{:toc}

## Azure Storage Connection Setup

After sign-up, select the Hybrid option and then the Azure Blob Storage provider.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.png" alt="Screenshot of the Hybrid provider selection">
</picture>

Provide your:
- Connection String
- Container Name

_For setting these up, see [Azure Setup](#azure-setup) below_
{: .fs-3 .text-grey-dk-000 }

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/connection-details.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/connection-details.png" alt="Screenshot of the Azure storage provider hybrid setup">
</picture>

'Save & Test' will attempt to write and read a file on the storage provider. Once tested, you will be asked to confirm the connection parameters.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/connection-confirm.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/connection-confirm.png" alt="Screenshot of the Azure storage provider hybrid setup confirmation">
</picture>

The solution is now connected to your Azure Storage.

## Azure Setup

These Azure setup instructions are provided as a template only. You should always fully understand your cloud environment setup and the security implications of making any changes. Please [get in touch]({% link docs/contact-us.md %}) if you have any concerns.
{: .warning }

### Storage Account & Container

Within the storage account service, create a new storage account.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/azure-create-account.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/azure-create-account.png" alt="Screenshot of creating a new storage account within Azure">
</picture>

Navigate to the newly created account and create a new storage container.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/azure-new-container.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/azure-new-container.png" alt="Screenshot of creating a new storage container within Azure">
</picture>

This storage container name is what needs to be provided within the [Azure Storage Connection Setup](#azure-storage-connection-setup).
{: .highlight }

### Access Keys

Navigate to the access keys for the storage account to retrieve the connection string.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/azure-keys.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/azure-keys.png" alt="Screenshot of retrieving the access key connection string for the storage account within Azure">
</picture>

This connection string is what needs to be provided within the [Azure Storage Connection Setup](#azure-storage-connection-setup).
{: .highlight }

## Testing

To test the solution, once the solution and hybrid connection is setup, navigate to the tickets view on the dashboard and select a ticket to extract the attachments for.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.png" alt="Screenshot of the Zendesk Storage Offload dashboard showing a ticket which has not yet been extracted">
</picture>

Now extract the ticket, the files will be shown within the Azure Storage Container

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/extracted-attachments.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/azure-storage/extracted-attachments.png" alt="Screenshot of the Azure Storage Container showing the extracted files">
</picture>


If you require an alternative file naming schema, please [get in touch]({% link docs/contact-us.md %})!