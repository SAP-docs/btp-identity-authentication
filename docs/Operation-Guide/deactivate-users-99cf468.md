<!-- loio99cf468fca3e43048af1734ed350478e -->

# Deactivate Users

As a tenant administrator, you can deactivate users in the administration console for SAP Cloud Identity Services.



<a name="loio99cf468fca3e43048af1734ed350478e__steps_adm_jxn_vdb"/>

## Procedure

1.  Sign in to the administration console for SAP Cloud Identity Services.

2.  Choose the *User Management* tile.

    The system displays the first 20 users in the tenant sorted by their user ID number.

3.  Find the user that you want to deactivate.

    For more information about how to find a user in Identity Authentication, see [Search Users](search-users-06078a6.md).

4.  Select the user that you want to deactivate.

    This operation opens the *User Details* view.

    ![](images/User_Details_in_Administration_Console_45ebcd1.png)

5.  **Optional:** Choose the *User Details* tab.

    1.  Expand the *Personal Information*

    2.  Press the edit icon ![](images/Edit_User_Details_e96801b.png) next to the *Personal Information* section.

    3.  Select *Inactive* from the dropdown next to the *Status* field.


6.  Save your changes.

    If the operation is successful, the system displays the message ***User <user ID\> updated***.




<a name="loio99cf468fca3e43048af1734ed350478e__result_lzp_b14_vdb"/>

## Results

When a user with status `Inactive` tries to log on to an application the following message appears: ***Sorry, we could not authenticate you. Try again.***

When a user is with a status `Inactive`, all actions in the *Password Details* page under the *Authentication* tab of *User Management* are disabled.

> ### Note:  
> To active a user again, set the *Status* to `Active`.

