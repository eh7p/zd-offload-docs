---
title: Security
layout: default
nav_order: 70
---

# Security

We take security extremely seriously and take a defence-in-depth layered approach to the security of our solution and infrastructure. We have outlined some common questions below however if you require any further information about our security practices then please do get in touch!

## Dashboard Authentication

All access to the dashboard and controls is protected through Zendesk's authorization and authentication flows within your Zendesk instance/subdomain. Additional access can be limited within the dashboard to prevent agents from making changes to the setup

## Sidebar App

All sidebar communication is routed through [Zendesk's proxy servers](https://developer.zendesk.com/documentation/apps/app-developer-guide/making-api-requests-from-a-zendesk-app/) and authenticated by your individual sidebar API key.

Attachment links within the sidebar app are time-restricted to prevent indefinite access.

## Cloud Storage

All our cloud storage is encrypted both over transit and at rest.