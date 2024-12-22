---
title: Google Cloud Storage Guide
layout: default
parent: Bring Your Own Storage (Hybrid)
---
# Google Cloud Storage
{: .no_toc }

1. TOC
{:toc}

## Google Cloud Storage Connection Setup

After sign-up, select the Hybrid option and then the Google Cloud Storage provider.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.png" alt="Screenshot of the Hybrid provider selection">
</picture>

Provide your:
- GCP Project ID
- Bucket name
- IAM User JSON key

_For setting these up, see [Google Cloud Setup](#google-cloud-setup) below_
{: .fs-3 .text-grey-dk-000 }

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/connection-details.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/connection-details.png" alt="Screenshot of the GCP provider hybrid setup">
</picture>

'Save & Test' will attempt to write and read a file on the storage provider. Once tested, you will be asked to confirm the connection parameters.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/confirm.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/confirm.png" alt="Screenshot of the GCP provider hybrid setup confirmation">
</picture>

The solution is now connected to your Google Cloud Storage.

## Google Cloud Setup

These Google Cloud setup instructions are provided as a template only. You should always fully understand your cloud environment setup and the security implications of making any changes. Please [get in touch]({% link docs/contact-us.md %}) if you have any concerns.
{: .warning }

### IAM Service User

From the IAM service, create a new service user for the solution to use to access the bucket

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/create-service-account.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/create-service-account.png" alt="Screenshot of creating a new service account within Google Cloud">
</picture>

Create a JSON key for the service account. 

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/create-key.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/create-key.png" alt="Screenshot of creating a JSON key for a service account within Google Cloud">
</picture>

This JSON key is what needs to be upload within the [Google Cloud Storage Connection Setup](#google-cloud-storage-connection-setup).
{: .highlight }

### Cloud Storage

Within the Cloud Storage service, create a new storage bucket

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/create-bucket.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/create-bucket.png" alt="Screenshot of creating a new storage bucket within Google Cloud">
</picture>

This bucket name is what needs to be provided within the [Google Cloud Storage Connection Setup](#google-cloud-storage-connection-setup).
{: .highlight }

Assign the new user the 'Storage Object Admin' permission from the bucket permissions

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/bucket-permission.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/bucket-permission.png" alt="Screenshot of assigning a user storage bucket permissions within Google Cloud">
</picture>


## Testing

To test the solution, once the solution and hybrid connection is setup, navigate to the tickets view on the dashboard and select a ticket to extract the attachments for.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.png" alt="Screenshot of the Zendesk Storage Offload dashboard showing a ticket which has not yet been extracted">
</picture>

Now extract the ticket, the files will be shown within the Google Cloud Storage Bucket

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/extracted-attachments.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/google-cloud-storage/extracted-attachments.png" alt="Screenshot of the Google Cloud Storage Bucket showing the extracted files">
</picture>


If you require an alternative file naming schema, please [get in touch]({% link docs/contact-us.md %})!