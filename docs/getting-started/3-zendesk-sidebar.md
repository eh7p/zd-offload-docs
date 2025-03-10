---
title: Zendesk Sidebar App Setup
layout: default
parent: Getting Started
nav_order: 3
---

# Zendesk Sidebar App Setup

The [sidebar app]({% link docs/sidebar-app.md %}) provides an interface within the Zendesk app to retain access to offloaded attachments.

Navigate to the [Sidebar App page on the Zendesk Marketplace](https://www.zendesk.com/marketplace/apps/support/1002546/attachment-storage-offload/){:target="_blank"} and install the application


<picture>
  <source type="image/webp" srcset="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/zd-marketplace.webp">
  <img alt="" src="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/zd-marketplace.png">
</picture>

When prompted, fill in the _apiToken_ value with your API Token, found on the [dashboard](https://zd-external-attachment-storage.eh7p.com/dashboard){:target="_blank"}


<picture>
  <source type="image/webp" srcset="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/app-install.webp">
  <img alt="" src="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/app-install.png">
</picture>

<picture>
  <source type="image/webp" srcset="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/dashboard-zd-sidebar-api.webp">
  <img alt="" src="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/dashboard-zd-sidebar-api.png">
</picture>

This API Token ensures that communication between the Zendesk app and our servers is secured.

The app is now setup to access offloaded attachments


<picture>
  <source type="image/webp" srcset="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/offloaded-ticket.webp">
  <img alt="" src="{{ site.baseurl }}/assets/images/docs/getting-started/zendesk-sidebar/offloaded-ticket.png">
</picture>

[Next - Finished Setup]({% link docs/getting-started/4-finished-setup.md %}){: .btn .btn-purple }

[Back - Offload Settings]({% link docs/getting-started/2-offload-settings.md %}){: .btn .btn-outline }