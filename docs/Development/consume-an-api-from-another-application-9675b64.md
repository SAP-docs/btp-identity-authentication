<!-- loio9675b64bc8014f4282e49d0cd8ce60fa -->

# Consume an API from Another Application

Define a dependency to the API of another application. Your consumer application can request an access token from Identity Authentication to consume that API.



<a name="loio9675b64bc8014f4282e49d0cd8ce60fa__prereq_dj5_ws3_m1c"/>

## Prerequisites

You know the name of the API from the provider application.

The provider applications must define this name automatically during deployment, in the documentation of the applications, or from the developers directly for custom developments.

For more information, see [Provide APIs for Consumption by Other Applications](provide-apis-for-consumption-by-other-applications-9d2fe83.md).



## Procedure

1.  Choose the consumer application.

2.  Choose the *Trust* tab.

3.  Under *Application APIs*, choose *Dependencies*.

4.  Enter the required data.

    1.  Enter a unique name for the dependency.

    2.  Choose the provider application and the API the consumer application consumes.


5.  Save your entries.




<a name="loio9675b64bc8014f4282e49d0cd8ce60fa__postreq_v1w_rw3_m1c"/>

## Next Steps

With the dependency name, the consumer application can call the `/token` endpoint of Identity Authentication. In the following example, the `resource` parameter uses the dependency name to identify the API that the consumer application consumes.

```
curl $iashost/oauth2/token  -X POST \
    -H 'Content-Type: application/x-www-form-urlencoded' \
    -H 'Accept: application/json' \
    -d "client_id=$clientid" \
    -d "client_secret=$secret" \
    -d "grant_type=urn%3Aietf%3Aparams%3Aoauth%3Agrant-type%3Ajwt-bearer" \
    -d "assertion=$IDTOKEN" \
    -d "resource=urn:sap:identity:application:provider:name:myDependency"
```

Identity Authentication returns an token with the access control for the APIs and audience claim. The following is an example of a token with the relevant claims.

```
{
    "ias_apis": [
        "sales-order"
    ],   
    "sub": "P123456",
    "mail": "donna.moore@example.com",
    "iss": "https://mytenant.accounts.ondemand.com",
    "last_name": "Moore",
    "aud": "1ab2cd3e-c573-4ad5-9007-28aa4e587a19", 
    "scim_id": "1a2345bc-4f6b-456b-9bfb-5d58beb97fb7",
    "user_uuid": "1a2345bc-4f6b-456b-9bfb-5d58beb97fb7",
    "azp": "e7c7e327-86c0-48a6-af57-a1234b567869",
    "exp": 1676989626,
    "iat": 1676986026,
    "first_name": "Donna",
    "jti": "123a45b6-a99e-47e0-b03d-b8c1304e8b42"
}
```

The consumer application sends this token to the API endpoint of the provider application, identified by the audience claim. The provider application can use the `ias_api` claim to decide if the consumer application can have access or rely on the authorizations of the user included in the token.

