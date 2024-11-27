---
title: Manual Offloading
layout: default
nav_order: 3
---

# Manual Offloading

Manual offloading can be useful for testing the solution.

Find a ticket which is valid for manual offloading and make a note of its ticket ID (in this case 18).

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/manual-offloading/valid-ticket.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/manual-offloading/valid-ticket.png" alt="">
</picture>

Next from the [dashboard](https://zd-external-attachment-storage.eh7p.com/dashboard){:target="_blank"}, navigate to the [tickets view](https://zd-external-attachment-storage.eh7p.com/dashboard){:target="_blank"}. From here input the ticket id or ticket URL and search for the ticket.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/manual-offloading/ticket-live.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/manual-offloading/ticket-live.png" alt="">
</picture>

Use the _Extract Attachments_ button to copy the attachment from Zendesk onto the Zendesk Storage Offload (or your storage if using the Hybrid solution) servers.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/manual-offloading/ticket-duplicated.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/manual-offloading/ticket-duplicated.png" alt="">
</picture>

Use the _Redact (Delete) from Zendesk_ button to remove the attachment from Zendesk.

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/manual-offloading/ticket-offloaded.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/manual-offloading/ticket-offloaded.png" alt="">
</picture>

Viewing this in Zendesk, you can see the attachment is now redacted, however can still be accessed through clicking the sidebar link (or via the dashboard on the tickets page)

<picture>
  <source srcset="{{ site.baseurl }}/assets/images/docs/manual-offloading/zd-offloaded.webp" type="image/webp">
  <img src="{{ site.baseurl }}/assets/images/docs/manual-offloading/zd-offloaded.png" alt="">
</picture>

The _Extract Attachments_ and _Redact (Delete) from Zendesk_ steps can be combined using the _Offload All Attachments_ Button.