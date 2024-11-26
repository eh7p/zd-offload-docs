---
title: Sidebar App
layout: default
nav_order: 3
---

# Sidebar App

The Sidebar App retains access for offloaded attachments directly in the Zendesk interface. Links to attachments are provided in the sidebar

![Image]({{ site.baseurl }}/assets/images/docs/sidebar-app/zd-offloaded.png)

In the [dashboard settings](https://zd-external-attachment-storage.eh7p.com/settings){:target="_blank"}, you can also modify whether the sidebar has offload controls, or is read-only.

![Image]({{ site.baseurl }}/assets/images/docs/sidebar-app/sidebar-controls.png)

Read more about [protecting attachments from being permanently deleted]({% link docs/protecting-attachments.md %})

All communications between the sidebar app and the backend goes via the [Zendesk Proxy server](https://developer.zendesk.com/documentation/apps/app-developer-guide/making-api-requests-from-a-zendesk-app/#making-a-request-to-a-third-party-api){:target="_blank"} and is protected with your personal API token.