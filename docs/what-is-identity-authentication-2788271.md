<!-- loio27882717f44b445fa287936c6f43dc1f -->

# What Is Identity Authentication?

 Authentication and single sign-on for users in the cloud. 

The Identity Authentication service provides you with controlled cloud-based access to business processes, applications, and data. It simplifies your user experience through authentication mechanisms, single sign-on, on-premise integration, and convenient self-service options.





### Authentication

-   All SAP Cloud applications can offer their users the same authentication mechanisms​

-   Strong authentication with configurable multi-factor \(MFA\) enforcement​
-   Easy separation mechanism for multiple user stores​
-   Flexible configuration where to validate user's credentials​



### Single Sign-On

-   Central SSO endpoint for all SAP Cloud applications
-   Pre-configured or semi-automated trust configuration



### Integrating SAP Applications

-   Common identity for users
-   Unified way for user management​
-   Security token service for protection of ​system-to-system communication
-   Data across applications can be correlated ​\(precondition for central foundation services\)​



## Environment

SAP Cloud Identity Services run on several underlying Infrastructure-as-a-Service technologies and regions. Some are owned by SAP and some are owned by our partner infrastructure providers, including Amazon Web Services \(AWS\) and Microsoft Azure. For more information, see [Regional Availability](regional-availability-be600ca.md).

Identity Authentication tenants run on the infrastructure of SAP Cloud Identity Services. You can find out more details about your tenant in the Administration Console of Identity Authentication.



## Features

 Authentication and SSO
 :   Choose one of the supported authentication methods to control access to your application, like Form, SPNEGO, Social, or two-factor authentication. Use SAML 2.0 protocol to provide single sign-on. Integrate your application programmatically using authentication via API.

  Configure Risk-Based Authentication
 :   Help enforce two-factor authentication based on IP ranges, user groups, user type, or authentication method to manage access to a business application.

  Delegate Authentication
 :   Delegate authentication to a 3rd party or on-premise IdP, as default or based on a condition like IdP, e-mail domain, user type or user group, and thus enable SSO across on-premise and the cloud.

  Use API
 :   Use SCIM REST API to manage users and groups, invite users, customize end-user UI texts in any language.

 

## Prerequisites

To use Identity Authentication, you must obtain a tenant. The tenant represents a single instance of the Identity Authentication that has a specific configuration and data separation.



## Tools

For configuration of most features, administrators use the administration console for Identity Authentication, which is a Fiori-based user interface adaptive to most browsers. For more information about the administration console, see [Operation Guide](Operation-Guide/operation-guide-6a8e67c.md).
