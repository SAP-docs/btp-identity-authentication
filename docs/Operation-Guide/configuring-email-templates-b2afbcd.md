<!-- loiob2afbcdccdf7410f8953e1e833e77de0 -->

# Configuring Email Templates

Tenant administrators can use the default or a custom email template set for the application processes.



## Overview

The email template set is a semantic grouping of different email templates. Each email template from the set is used for the respective application process, such as self-registration, for example. When a user makes a registration for an application, Identity Authentication uses the email template for self-registration from the template set to communicate with that user.

The administration console for SAP Cloud Identity Services provides the possibility to use a default email template set with English templates only. The default set is named *Default*.

You can also configure your own templates in a custom template set. There you can customize the texts and branding according to your needs.

You can define a set of email templates with different language versions for the following processes:


<table>
<tr>
<th valign="top">

Email Template

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

Self-Registration

</td>
<td valign="top">

This email template is used when a user registers via the Registration page. The user then receives an email with instructions about how to activate his or her account. The name of the email template used for this process is *Self-Registration*.

</td>
</tr>
<tr>
<td valign="top">

On-Behalf Registration

</td>
<td valign="top">

This email template is used when somebody else registers the user on his or her behalf via the import user option for Identity Authentication. In this case, the registered user receives an email with instructions about how to activate his or her account. The name of the email template used for this process is *On-Behalf Registration.* 

</td>
</tr>
<tr>
<td valign="top">

Invitation

</td>
<td valign="top">

This email template is used when a user invites another user for registration via the Invitation REST API. In this case, the invitee receives an email with instructions about how to register. The name of the email template used for this process is *Invitation*.

</td>
</tr>
<tr>
<td valign="top">

Forgot Password

</td>
<td valign="top">

This email template is used when:

-   a user wants to change his or her password by going through the Forgot Password page. In this case, the user receives an email with instructions about how to change his or her password. The name of the email template used for this process is *Forgot Password*.

-   an administrator sends a reset password email via the administration console. For more information, see [Send Reset Password Email](send-reset-password-email-da55abf.md).



</td>
</tr>
<tr>
<td valign="top">

Locked Password

</td>
<td valign="top">

This email template is used when a user locks his or her password by exceeding the allowed number of logon attempts. In this case, the user receives an email with instructions about how to log on. The name of the email template used for this process is *Locked Password*.

</td>
</tr>
<tr>
<td valign="top">

Reset Password

</td>
<td valign="top">

This email template is used when: a user has to reset his or her password. In this case, the user receives an email with instructions about how to reset his or her password.

The name of the email template used for this process is *Reset Password*.

The email template for *Reset Password* process are used when the process is triggered from the system, based on the password policy \(for example, the user's password length is not enough according to the password policy requirements\) and the user receive reset password notification email.

</td>
</tr>
<tr>
<td valign="top">

Deactivate TOTP Device

</td>
<td valign="top">

This email-template is used when a user has requested to receive a passcode via email. The passcode is used to deactivate the devices used to generate passcodes for TOTP Two-Factor Authentication. The name of the email template used for this process is *Deactivate TOTP Device*.

</td>
</tr>
<tr>
<td valign="top">

Email OTP Code

</td>
<td valign="top">

This email-template is used when a user has requested to receive an 8-digit code via email. The user needs the code for two-factor authentication.

</td>
</tr>
<tr>
<td valign="top">

Send Security Alert

</td>
<td valign="top">

This email-template is used when the user's password is set, changed, or reset, the email, or login name is changed, or when TOTP or Web TFA devices are activated or deactivated. The name of the email template used for this process is *Send Security Alert*.

> ### Note:  
> The sending of security alert emails is switched off by default. For more information, see [Send Security Alert Emails](send-security-alert-emails-c977464.md).



</td>
</tr>
</table>

To activate a user registration or to reset a password, users choose links sent to them in the emails. For these cases, you can use placeholders. For more information about which placeholders can be used, see [Edit or Add an Email Template Set](edit-or-add-an-email-template-set-3c4f397.md).

> ### Restriction:  
> If you select a corporate identity provider, the option to configure email templates is not possible. In this case you can access only some of the custom configurations for the applications. The configurations under the *Authentication and Access* and *Branding and Layout* tabs are partially visible. For more information, see [Choose Default Identity Provider for an Application](choose-default-identity-provider-for-an-application-e9d8274.md).

You can also define which languages each email template uses, and you can set custom versions for each language. You can set the following languages:

Arabic, Azerbaijani, Bulgarian, Catalan, Chinese \(PRC\), Chinese \(Taiwan\), Croatian, Czech, Danish, Dutch, English \(United Kingdom\), English \(United States\), Estonian, Finnish, French \(Standard\), French \(Canada\), German \(Standard\), Greek, Hebrew, Hungarian, Italian, Japanese, Korean, Latvian, Malay, Norwegian, Polish, Portuguese \(Portugal\), Romanian, Russian, Serbian, Slovak, Slovenian, Spanish \(Spain\), Spanish \(Mexico\), Swedish, Thai, Turkish, Ukrainian, Vietnamese, Welsh.



The language for the email template sets is set according to the following order of priorities:

**User request flow** - when the user requests a process, for example Forgot Password, the emails use the language that the user's browser is set to.

-   If the language isn't in the list of supported languages, the emails use *English*.

-   If the language is in the list of supported languages, but there isn't a template for that language, the emails use English.

-   If the language is in the list of supported languages, and there is a template for that language, the emails use this language.


**System request flow** - for example when the administrator chooses the Reset Password option in the administration console, the emails use the language set in the profile of the user. If there isn't a template for that language, the emails use *English* instead.



If you want to use a custom email template you should create one if it doesn't exist. Add or edit the email template set, if necessary, and then define that email template set for the application. To add or edit the email template, first you must open the uploaded email templates, and then save a copy. Optionally you can delete an email template set or a language version for a specific application process.



You can perform the following steps:

