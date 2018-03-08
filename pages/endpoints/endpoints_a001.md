---
title: A001 Create Professional Session
sidebar: overview_sidebar
permalink: endpoints_a001.html
summary: "A001 Create Professional Session."
---

# A001 Create Professional Session

## API
[POST /v1/ProfessionalSession](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/professionalsession/createProfessionalSessionUsingPOST){:target="_blank"}

## Description
Creates a Professional Session in the Spine using smartcard roles. This gives a secure login.

## Input
[Professional Session Resource](https://developer.nhs.uk/library/systems/e-rs/ecosystem/explore/resources/professionalsession/){:target="_blank"}

Provide only a token when first creating a session.

### Example
```javascript
{
 "token": "<token id>"
}
```

## Output
The created [Professional Session Resource](https://developer.nhs.uk/library/systems/e-rs/ecosystem/explore/resources/professionalsession/){:target="_blank"} will be returned with available user permissions populated.

## Code Sample
Code snippets taken from the consumer example. See [Code Samples](https://developer.nhs.uk/library/systems/e-rs/ecosystem/develop/code/){:target="_blank"} for further details.

```javascript
function createSession(tokenCode, entryUrl) {
     scope.entryUrl = entryUrl;
     var json = {
         token: tokenCode
     };
     var deferred = $q.defer();
 
     var headersJson = {};
     headersJson[config.asidHeader] = config.asid;
 
     var rest = $resource(
             config.baseUrl + '/v1/ProfessionalSession',
             null,
             {'save': {method: 'POST', headers: headersJson}}
     );
     rest.save(json, function (data) {
         scope.sessionData = data;
         scope.currentSessionId = data.id;
         deferred.resolve(data);
     });
     return deferred.promise;
 }
```

## Notes
Once the session has been created a list of applicable permissions for the user will be returned. The session will not be usable until a permission/role has been selected using the Select Role endpoint.

The ProffessionalSession.id returned should be included as a header (HTTP_X_SESSION_KEY) for all subsequent requests.

### Response Messages
