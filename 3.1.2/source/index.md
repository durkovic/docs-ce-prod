# Gluu Server Community Edition (CE) 3.1.2 Documentation
## Introduction
The Gluu Server is a container distribution of free open source identity and access management (IAM) software. With a Gluu Server, you can offer a central authentication and authorization service for many SaaS, custom, open source and commercial web and mobile applications.  

The most common use cases for the Gluu Server include:

- Single sign-on (SSO)   
- Mobile authentication    
- API access management  
- Two-factor authentication 
- Customer identity and access management (CIAM)   
- Identity federation      

### Open Standards
The Gluu Server includes software that implements open web standards for authentication, authorization, federated identity, and identity management:

- OAuth 2.0    
- SAML 2.0   
- OpenID Connect    
- User Managed Access 2.0 (UMA)    
- System for Cross-domain Identity Management (SCIM)    
- FIDO Universal 2nd Factor (U2F)    
- Lightweight Directory Access Protocol (LDAP)   

### Free Open Source Software
All software included in the Gluu Server distribution is free open source software that can be used in production for free. Learn more about the open source licenses in use [below](#license). 

## Installation
The Gluu Server can be installed on the cloud provider of your choice using one of our Linux packages for Ubuntu, CentOS, RHEL and Debian. Follow our [VM preparation guide](./installation-guide/index.md) to get started. 

## Directory Service
All data used and generated by the Gluu Server is stored in the local Gluu LDAP deployed during installation. The LDAP includes complete details about OpenID Connect and UMA clients, user objects, and more. Learn more in the [user management guide](./user-management/local-user-management.md)

If there is an existing Active Directory or backend LDAP server, data can be synced to Gluu using the [Cache Refresh process](./user-management/ldap-sync.md). 

!!! Note
    The Gluu Server always needs identity data stored locally. 

## Identity Management
Via the "oxTrust" admin interface, and using an LDAP browser, identity and object data such as user profiles, configuration data, tokens and credentials can be managed. 

If you have an existing identity management platform, or have written your own identity management tool(s), identity data can be sent to Gluu using the [SCIM protocol](./user-management/scim2.md). 

The Gluu Server does **not** include features for delegated administration, role definition, approvals and workflows, etc. In enterprise workflows, the Gluu Server is a consumer of separate systems that house identity management and governance data and policies. 

##  Single Sign-On (SSO)
The Gluu Server is an identity provider (IDP) in single sign-on (SSO) workflows. Users from web and mobile applications are redirected to Gluu for "sign-on", and are then redirected back to applications with an active session and claims (or attributes) about themselves. 

Learn how to configure the Gluu Server's [OpenID Connect Provider (OP)](./admin-guide/openid-connect.md) and [SAML Identity Provider (IDP)](./admin-guide/saml.md) in the admin guide.

Learn how to secure and integrate web and mobile apps in the [SSO integration guide](./integration/index.md).

## Strong Authentication
A central authentication system like Gluu enables strong authentication to be enforced for many applications in one place. The Gluu Server was designed to support a wide range of authentication mechanisms and custom business logic for how authentication should be applied during the user sign-in process. 

Learn how to configure the Gluu Server's out-of-the-box and custom strong authentication options in the [authentication guide](./authn-guide/intro.md). 

## Access Management
The Gluu Server supports the User Managed Access (UMA) 2.0 profile of OAuth 2.0, which provides a RESTful, JSON-based approach to coordinating the protection of APIs and web resources. UMA does not standardize a policy expression language, enabling flexibility in policy expression and evaluation through XACML, other declarative policy languages, or procedural code as warranted by conditions.

Learn more about using the Gluu Server for access management in the [UMA docs](./admin-guide/uma.md).

## Support
Gluu offers free and VIP support! Anyone can browse or register and post questions on the [Gluu support portal](https://support.gluu.org). Tickets opened by the community are public, and we do our best to answer them in a timely manner. 

Private support, guaranteed response times, and consultative support are available with a paid support contract. For more information, see [our website](https://gluu.org/pricing).

## Contribute 
We want to keep improving our docs. Please help us improve by submitting
any improvements to our [Documentation Github](https://github.com/GluuFederation/docs-ce-prod).
If you're a Github pro, submit a pull request. If not, just open an issue
on any typos, bugs, or improvements you'd like to see. We need your
help... even if you're not a coder, you can contribute! 

## License
The Gluu Server is a container distribution composed of software written by Gluu and incorporated from other open source projects. Gluu
projects are frequently prefixed with our open source handle: **ox** (e.g. oxAuth, oxTrust). Any code in the Gluu Server that we wrote is MIT license, and is available on [Github](https://github.com/GluuFederation/). The license for each software component is listed below.

|	Component	|	License	            |
|-----------------------|---------------|
|	oxAuth      | [MIT License](http://opensource.org/licenses/MIT)|
|	oxTrust      | [MIT License](http://opensource.org/licenses/MIT)|
|	Shibboleth IDP      | [Apache2](http://www.apache.org/licenses/LICENSE-2.0)|
|   OpenDJ              | [CDDL](https://opensource.org/licenses/CDDL-1.0)
|	OpenLDAP	        | [OpenLDAP Public License](http://www.openldap.org/software/release/license.html)|
| Passport-JS           | [MIT License](https://github.com/jaredhanson/passport/blob/master/LICENSE) |
|  UnboundID LDAP SDK	| [UnboundID LDAP SDK Free Use License](https://github.com/UnboundID/ldapsdk/blob/master/LICENSE-UnboundID-LDAPSDK.txt)|
| Jetty / Apache HTTPD  | [Apache2](http://www.apache.org/licenses/LICENSE-2.0)|
|	Asimba		        | [GNU APGL 3.0](http://www.gnu.org/licenses/agpl-3.0.html)|