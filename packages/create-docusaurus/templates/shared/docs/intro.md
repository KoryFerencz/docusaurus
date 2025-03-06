---
sidebar_position: 1
---

# Authentication

Getting started for Client Integrations with MasterMind**.

## How to get access to the MasterMind API

The tenant’s environment(s) must be created to access the MasterMind Ingress API URLs. (ie: api.test.<tenant>.mastermindtms.com). The Technical Program Manager and IMPL Project Manager are responsible for requesting Environment build and target timelines.

They are able to access Mastery Test’s API Documentation in the interim https://api.test.mm100.mastermindtms.com/docs/v2

The tenant’s developers can proactively access Mastery’s API Developer Portal before the non-production environments are created.**.



## EXTERNAL: Request Github MasterMind API Portal Acces

1. Solution Architects or Engagement Project Managers will request individual Github handles from Client - if the Clients do not have Github handles they can create them for free on github’s website
2. Once github handles are received, SA or Engagement Project Manager will submit an Internal Service Desk request for Access specifying the customer’s developer(s) Github handle - this can be done through a general request including the following information:
   a. Client user’s Github handles
   b. Users email address
   c. This link (https://github.com/masterysystems/api-developer-portal/wiki/1.-MasterMind-API#getting-started) and include this message: “Please grant restricted access to the above github users to this API Developer wiki page. This wiki page will be referenced by our Client’s developers as they start to make connectivity with the External API / Event Hub. They should not be granted access to any internal github repositories. 
3. Client’s users will receive an email with authentication steps to follow. Once completed, they will have access to Mastermind API Developer Portal
4. Any troubleshooting that needs to occur should go through Service Desk

### This portal will provide tenant’s access to:

1. Getting Started Steps
2. API Authentication Information
3. MasterMind Standard Naming Conventions & Best Practices
4. API Error Handling Guides that accomany the errors they will receive in Minion - API Dashboard and/or the Ingress Reply Topics
5. Mastery’s API Versioning
6. MasterMind’s Event Hubs API Reference Index (includes the Topic schema)

## EXTERNAL: Request External 1Password Vault for Client

1Password is used to share secure information, like credentials, with Mastery Clients.  An external 1Password vault will be used to share MasterMind API & Event Hub credentials with the Clients and for Clients to share their API or 3rd Party Credentials based on their solutions.

Credentials should not be shared via email, messaging portals, etc. All secure information must be shared via 1Password

Note: Credentials must be copied to or from the external vault to the client’s internal vault. must be copied from the Client’s internal 1password vault and/or copied from inter

1. After kick-off, Engagement Project Managers will request single email address (typically a shared distribution list) from Client that will be used to access 1Password. If they require individual, Client will need to request a full list of email addresses. Note: Clients should only be giving permissioned users access to 1password - this is a security item.
2. Once email addresses are received, the Engagement Project Manager to request an External Vault to be created. This request must include the email address(s) noted above. This can happen before the new environment build occurs

## EXTERNAL: Provide Client with API & Event Hub Credentials

MasterMind API Setup

Prior to a Tenant invoking MasterMind APIs, they will need access to the API credentials. There will be unique credentials between non-production and production environments. 

1. As part of the New Environment Build process, API credentials and Event Hub connection strings should be copied to the Client’s External 1Password vault
        a. Engagement Project Managers should include the following verbiage as part of “handing over” the environments to Clients
        b. Ingress API Credentials include:  Client ID, Client Secret and Token URL.
            i. Example Credentials:
                1. Client ID: test.<tenant>.mastermindtms.com-default-external-ingress
                2. Client Secret: XXXXXXX
                3. Token URL: https://id.<tenant>.mastermindtims.com/auth/realms/<environment>.<tenant>.mastermindtms.com/protocol/openid-connect/token
