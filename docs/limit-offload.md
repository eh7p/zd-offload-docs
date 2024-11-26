---
title: Limit Offloading
layout: default
nav_order: 4
---

# Limiting Offloads

The settings page, accessible from the [dashboard](https://zd-external-attachment-storage.eh7p.com/dashboard), provides many options for limiting which attachments are offloaded.

![Image]({{ site.baseurl }}/assets/images/docs/limit-offload/ticket-settings.png)

## Limit automatic offloading

Automatic offloading can be enabled/disabled. When disabled [manual offloading]({% link docs/manual-offloading.md %}) is still possible and previously offloaded attachments are still available.

## Limit by ticket close date

Offloading can be limited to only occur once a ticket has remained closed for a set number of days.

## Limit by total offload

Stop offloading once the total extracted amount exceeds this value.

## Limit by amount remaining in zendesk

Stop offloading once the total amount remaining in Zendesk is less than this value. Set this to below your Zendesk included file storage limit to prevent incurring additional Zendesk storage fees.

## Limit by attachment size

Don't offload attachments which are smaller than a given size.

## Limit by attachment filetype

Only extract attachments with the provided filetypes

## Limit by inline atttachments

Whether or not to offload [inline attachments](https://support.zendesk.com/hc/en-us/articles/4408832757146-Enabling-attachments-in-tickets). Offloading inline attachments will prevent end-users from accessing these.