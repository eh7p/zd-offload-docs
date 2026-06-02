---
title: End User Visibility
layout: default
nav_order: 7
---

# End User Visbility

Depending on your Zendesk configuration and specific attachments, end-user visibility of attachments may be affected once attachments are offloaded.

Attachments differ in type between:
- Email Attachment, attached in addition to the email, appears in the header/footer
- Inline Attachment, attached inline within the body of the email (for instance an image)
- Linked Attachment, used by Zendesk when outbound file exceeds 7MB or total outbound size across all attached files exceeds 10MB

Because linked attachments are hosted by Zendesk, these are not visible to end-users once they have been offloaded. You can read more about [Linked attachments on Zendesk's help site](https://support.zendesk.com/hc/en-us/articles/4408832757146-Allowing-attachments-in-tickets#topic_lv2_cnx_xdb).

|                   | Email Attachment | Inline Attachment | Linked Attachment |   |
|-------------------|------------------|-------------------|-------------------|---|
| End-User -> Agent | Visible          | Visible           | N/A               |   |
| Agent -> End-User | Visible          | Visible           | Not Visible       |   |

Attachments sent from the end-user to agents are always visible to the end-user.

## Private Attachments

If you have [private attachments](https://support.zendesk.com/hc/en-us/articles/4408832757146-Allowing-attachments-in-tickets#topic_nrp_bnx_xdb) enabled in your Zendesk instance, users will be required to sign-in to view attachments that have been sent from you to the end-user.

Once attachments are offloaded, they will no longer be visible to end-users.
Attachments sent from the end-user to agents are always visible to the end-user.

