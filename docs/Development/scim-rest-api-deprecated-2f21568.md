<!-- loio2f215687fcf34170b0bbc8b36b60f2e9 -->

# SCIM REST API \(Deprecated\)

This section contains information about the Identity Authentication implementation of the System for Cross-domain Identity Management \(SCIM\) REST API protocol.



> ### Note:  
> This API is deprecated. Please use [Identity Directory SCIM REST API](https://api.sap.com/api/IdDS_SCIM/overview) instead. For more information, see [Migrating Identity Authentication SCIM REST API to Identity Directory Service API](migrating-identity-authentication-scim-rest-api-to-identity-directory-service-api-106dbe0.md).



## Prerequisites

To call the methods of this SCIM REST API you must have a system as administrator with an assigned *Manage Users* role. For more details about how to add a system as administrator and assign administrator roles, see [Add System as Administrator](../Operation-Guide/add-administrators-bbbdbdd.md#loiocefb742a36754b18bbe5c3503ac6d87c), and [Edit Administrator Authorizations](../Operation-Guide/edit-administrator-authorizations-86ee374.md).



<a name="loio2f215687fcf34170b0bbc8b36b60f2e9__additional_supported_values"/>

## Additional Attributes Supported Values

Some of the attributes have predefined supported values. They are returned as a map of key value pairs. See some examples in the table below. For the full set of attributes, copy the URL from the table, replace <Cloud Identity Services domain\> with the correct one, and open the edited URL in a web browser.

> ### Note:  
> The domain part has the following pattern:
> 
> `<tenant ID>.accounts.ondemand.com` or `<tenant ID>.accounts.cloud.sap`. If you have a configured custom domain, the domain has the following pattern: <your custom domain\>.
> 
> *Tenant ID* is an automatically generated ID by the system. The first administrator created for the tenant receives an activation email with a URL in it. This URL contains the *tenant ID*. For more information about your tenants, see [View Assigned Tenants and Admins](../view-assigned-tenants-and-admins-f56e6f2.md).


<table>
<tr>
<th valign="top">

Attribute

</th>
<th valign="top">

Examples

</th>
<th valign="top">

Full Sets

</th>
</tr>
<tr>
<td valign="top">

`name.honorificPrefix` 

</td>
<td valign="top">

-   \[Mr., Ms.\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/salutations</code>**




</td>
</tr>
<tr>
<td valign="top">

`addresses.country` 

</td>
<td valign="top">

-   \[AF, AX\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/countries</code>**




</td>
</tr>
<tr>
<td valign="top">

`addresses.region` 

</td>
<td valign="top">

-   \[NY\]

-   \[AB\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/states/us</code>**

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/states/ca</code>**




</td>
</tr>
<tr>
<td valign="top">

`industryCrm` 

</td>
<td valign="top">

-   \[Aerospace and Defense\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/industries</code>**




</td>
</tr>
<tr>
<td valign="top">

`timeZone` 

</td>
<td valign="top">

-   \[Africa/Abidjan\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/timezones</code>**




</td>
</tr>
<tr>
<td valign="top">

`department` 

</td>
<td valign="top">

-   \[Administration\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/departments</code>**




</td>
</tr>
<tr>
<td valign="top">

`companyRelationship` 

</td>
<td valign="top">

-   \[Consultant\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/relationships</code>**




</td>
</tr>
<tr>
<td valign="top">

`locale` 

</td>
<td valign="top">

-   \[EN\]




</td>
<td valign="top">

-   **<code>https://&lt;Cloud Identity Services domain&gt;/md/languages</code>**




</td>
</tr>
</table>



<a name="loio2f215687fcf34170b0bbc8b36b60f2e9__section_m2y_xz5_xcb"/>

## Restricted Characters

The characters `<`, `>`, `:` are not allowed for the attributes `displayName`, `name.familyName`, and `name.givenName`.



<a name="loio2f215687fcf34170b0bbc8b36b60f2e9__section_mh4_lh2_nbb"/>

## Methods



**Manage Users**


<table>
<tr>
<th valign="top">

HTTP Method

</th>
<th valign="top">

Action

</th>
<th valign="top">

URI

</th>
</tr>
<tr>
<td valign="top">

*GET*

</td>
<td valign="top">

[Users Search \(Deprecated\)](users-search-deprecated-3af7dfa.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Users/</code>**

</td>
</tr>
<tr>
<td valign="top">

*GET*

</td>
<td valign="top">

[User Resource \(Deprecated\)](user-resource-deprecated-7ae17a6.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Users/&lt;id&gt;</code>**

</td>
</tr>
<tr>
<td valign="top">

*POST*

</td>
<td valign="top">

[Create User Resource \(Deprecated\)](create-user-resource-deprecated-cea8778.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Users</code>**

</td>
</tr>
<tr>
<td valign="top">

*PUT*

</td>
<td valign="top">

[Update User Resource \(Deprecated\)](update-user-resource-deprecated-9e36479.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Users/&lt;id&gt;</code>**

</td>
</tr>
<tr>
<td valign="top">

*DELETE*

</td>
<td valign="top">

[Delete User Resource \(Deprecated\)](delete-user-resource-deprecated-436015d.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Users/&lt;id&gt;</code>**

</td>
</tr>
</table>

**Manage Groups**


<table>
<tr>
<th valign="top">

HTTP Method

</th>
<th valign="top">

Action

</th>
<th valign="top">

URI

</th>
</tr>
<tr>
<td valign="top">

*GET*

</td>
<td valign="top">

[Groups Search \(Deprecated\)](groups-search-deprecated-77e6811.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Groups/</code>**

</td>
</tr>
<tr>
<td valign="top">

*GET*

</td>
<td valign="top">

[Group Resource \(Deprecated\)](group-resource-deprecated-8c6ebd7.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Groups/&lt;id of the group&gt;</code>**

</td>
</tr>
<tr>
<td valign="top">

*POST*

</td>
<td valign="top">

[Create Group Resource \(Deprecated\)](create-group-resource-deprecated-a831c94.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Groups</code>**

</td>
</tr>
<tr>
<td valign="top">

*PUT*

</td>
<td valign="top">

[Update Group Resource \(Deprecated\)](update-group-resource-deprecated-81ca50e.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Groups/&lt;id of the group&gt;</code>**

</td>
</tr>
<tr>
<td valign="top">

*DELETE*

</td>
<td valign="top">

[Delete Group Resource \(Deprecated\)](delete-group-resource-deprecated-41bb519.md)

</td>
<td valign="top">

**<code>https://&lt;Cloud Identity Services domain&gt;/service/scim/Groups/&lt;id of the group&gt;</code>**

</td>
</tr>
</table>

**Related Information**  


[SAP Cloud Identity Services Application Directory REST API](sap-cloud-identity-services-application-directory-rest-api-a8fc935.md "Manage application configurations.")

[Identity Directory SCIM REST API](identity-directory-scim-rest-api-5be5692.md "Manage users, groups and custom schemas in the cloud.")

[Invitation REST API](invitation-rest-api-e55429f.md "The invitation service allows you to implement a request for user invitations.")

[User Management REST API](user-management-rest-api-e6bb70d.md "This REST API allows you to implement a request for user management, such as user registration, as well as SP user retrieval, deactivation and deletion.")

[Password Service REST API](password-service-rest-api-8d1016b.md "The password service is used for operations related to user passwords, such as verification of the user name and the password combination.")

[Forgot Password REST API](forgot-password-rest-api-d024fca.md "The forgot password REST API sends a reset password email.")

[TOTP Validation Service](totp-validation-service-3e4c3cf.md "Validation of time-based one-time password (TOTP).")

[Change Tenant Texts REST API](change-tenant-texts-rest-api-66ad80a.md#loio66ad80a6bbaf4fc3911232f7cc9a7de6 "The Change Tenant Texts REST API of Identity Authentication can be used to change the predefined texts and messages for end-user screens available per tenant in the Identity Authentication.")

[Change Master Data Texts REST API](change-master-data-texts-rest-api-b10fc6a.md#loiob10fc6a9a37c488a82ce7489b1fab64c "The Change Master Data Texts REST API can be used to change the predefined master data for each resource in Identity Authentication.")

[System for Cross-Domain Identity Management](https://tools.ietf.org/html/draft-ietf-scim-api-19)

[SCIM Data Types](https://tools.ietf.org/html/rfc7643#section-2.3)

