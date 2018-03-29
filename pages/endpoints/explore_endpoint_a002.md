---
title: A002 Professional Session Select Role
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: /explore_endpoint_a002.html
summary: false
---

## API
[PUT /v1/ProfessionalSession/{sessionKey}](https://api.dev1.ers.ncrs.nhs.uk/ers-api/v1/ProfessionalSession/pro-xapi-session_94414701-70d0-4570-a674-f6f2125ab571)

## Description
Updates a Professional Session with the appropriate NHS organisation and role. This ensures the correct access rights for the user.

## Input
[Professional Session Resource](explore_models.html)

The base input for this endpoint should be the output from the Create Session endpoint. The consumer should then additionally populate the permission field with the permission they wish to select from those available to the user (ProfessionalSession.user.permissions).

### Example
```javascript
{
    "id": "pro-xapi-session_0537f534-5c9a-4240-a401-90c9b7770139",
    "token": "<token id>",
    "user": {
        "identifier": "021600556514",
        "firstName": "Tech",
        "lastName": "Support",
        "middleName": null,
        "permissions": [
        {
            "businessFunction": "REFERRING_CLINICIAN_ADMIN",
            "orgIdentifier": "R68",
            "orgName": "BTL NHS TRUST R68"
        },
        {
            "businessFunction": "REFERRING_CLINICIAN",
            "orgIdentifier": "R69",
            "orgName": "BTL NHS TRUST R69"
        },
        {
            "businessFunction": "REFERRING_CLINICIAN_ADMIN",
            "orgIdentifier": "R69",
            "orgName": "BTL NHS TRUST R69"
        }]
    },
    "permission": {
        "businessFunction": "REFERRING_CLINICIAN",
        "orgIdentifier": "R69",
        "orgName": "BTL NHS TRUST R69"
    }
}
```

## Output
The created [Professional Session Resource](explore_models.html) will be returned with with the selected permission applied.

## Code Sample
Code snippets taken from the consumer example. See [Code Samples](develop_code_samples.html) for further details.

```javascript
function selectRole(permission) {
     var deferred = $q.defer();
     scope.selectedPermission = permission;

     var headersJson = {};
     headersJson[config.asidHeader] = config.asid;
     headersJson[config.sessionIdHeader] = scope.sessionData.id;

     var rest = $resource(config.baseUrl + '/v1/ProfessionalSession/' + scope.currentSessionId,
             null,
             {
                 'save': {method: 'PUT', headers: headersJson}
             });
     var json = {
         id: scope.sessionData.id,
         permission: permission
     };
     rest.save(json, function (data) {
         deferred.resolve(data);
     });

     return deferred.promise;
 }
```

## Notes
The Create Session endpoint must be called in order to create the session. This endpoint can then be used to select one of the applicable roles/permissions returned.

The ProfessionalSession.id returned from the Create Session endpoint should be included as a header (HTTP_X_SESSION_KEY) for this and all subsequent requests.
