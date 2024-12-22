---
title: AWS S3 Storage Guide
layout: default
parent: Bring Your Own Storage (Hybrid)
---
# AWS S3 Storage
{: .no_toc }

1. TOC
{:toc}

## AWS Connection Setup

After sign-up, select the Hybrid option and then the AWS S3 Storage provider.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/select-provider.png" alt="Screenshot of the Hybrid provider selection">
</picture>

Provide your:
- IAM Key
- IAM Secret
- AWS Region
- Bucket Name

_For setting these up, see [AWS Setup](#aws-setup) below_
{: .fs-3 .text-grey-dk-000 }

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/connection-details.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/connection-details.png" alt="Screenshot of the AWS S3 provider hybrid setup confirmation">
</picture>

'Save & Test' will attempt to write and read a file on the storage provider. Once tested, you will be asked to confirm the connection parameters.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/confirm.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/confirm.png" alt="Screenshot of the AWS S3 provider hybrid setup confirmation">
</picture>

The solution is now connected to your AWS S3 Storage.

## AWS Setup

These AWS setup instructions are provided as a template only. You should always fully understand your cloud environment setup and the security implications of making any changes. Please [get in touch]({% link docs/contact-us.md %}) if you have any concerns.
{: .warning }

### Bucket Creation

From the S3 service, create a new bucket.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-bucket.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-bucket.png" alt="Screenshot of creating an S3 bucket within AWS">
</picture>

This bucket and region are what need to be provided within the [AWS Connection Setup](#aws-connection-setup).
{: .highlight }

### IAM Setup

Within the IAM service, create an IAM policy for bucket access. The policy should have the following permissions

```json
 {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:ListBucket",
                "s3:GetObject",
                "s3:DeleteObject",
                "s3:GetObjectAcl",
                "s3:PutObjectAcl",
                "s3:PutObject"
            ],
            "Resource": [
                "arn:aws:s3:::your-bucket-name",
                "arn:aws:s3:::your-bucket-name/*"
            ]
        }
    ]
}
```

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-iam-policy.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-iam-policy.png" alt="Screenshot of creating a new IAM policy within AWS - JSON">
</picture>
<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-iam-policy-2.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-iam-policy-2.png" alt="Screenshot of creating a new IAM policy within AWS - Details">
</picture>

Next create a new IAM user for the solution to use to access the bucket

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-iam-user.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-iam-user.png" alt="Screenshot of creating a new IAM user within AWS">
</picture>

Assign the previously created policy to the new user

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/assign-policy.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/assign-policy.png" alt="Screenshot of assigning the IAM policy to the User within AWS">
</picture>

Once the user is created, create a new access key for the user. Select the 'Other' use case. When prompted copy the newly created access key secret.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-access-key.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/create-access-key.png" alt="Screenshot of creating a new access key for the use within AWS">
</picture>

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/access-key-created.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/access-key-created.png" alt="Screenshot of a new access key for the use within AWS">
</picture>

This access key and secret access key are what need to be provided within the [AWS Connection Setup](#aws-connection-setup).
{: .highlight }


## Testing

To test the solution, once the solution and hybrid connection is setup, navigate to the tickets view on the dashboard and select a ticket to extract the attachments for.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/19-pre-extract.png" alt="Screenshot of the Zendesk Storage Offload dashboard showing a ticket which has not yet been extracted">
</picture>

Now extract the ticket, the files will be shown within the AWS S3 bucket

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/extracted-attachments.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/bring-your-own-storage/aws-storage/extracted-attachments.png" alt="Screenshot of the S3 bucket showing the extracted files">
</picture>




If you require an alternative file naming schema, please [get in touch]({% link docs/contact-us.md %})!