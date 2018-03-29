---
title: "A004: Retrieve Reference Data"
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: explore_endpoint_a004.html
summary: false
---

## API
[GET /v1/ValueSet/{valueSetId}](https://api.dev1.ers.ncrs.nhs.uk/ers-api/v1/ValueSet/valueSetId)

## Description
This read-only API lets a user access a pre-populated list of reference data. The NHS e-Referral Service uses these lists throughout. For example, a list of specialities. They support data accuracy and effective re-use. It retrieves a specific Value Set (Reference Dataset) by ID.

## Input
Applicable values for the {valueSetId}:

|Value Set ID|Description|
|---|---|
|REQUEST_PRIORITY|Request Priorities defined in e-RS.|
|SPECIALTY|Specialties defined in e-RS. Also returns applicable Clinic Types as sub-concepts (categorized by Specialty).|
|CLINIC_TYPE|Clinic Types defined in e-RS.|
|REQUEST_TYPE|Request Types defined in e-RS.|
|COMMISSIONING_TYPE|Commissioning Types defined in e-RS.|

## Output
A [Value Set Resource](explore_models.html) profiled specifically for the given valueSetId. This will include the requested coding system with its available codes.

## Code Sample
Code snippets taken from the consumer example. See [Code Samples](https://developer.nhs.uk/library/systems/e-rs/ecosystem/develop/code/) for further details.

```javascript
angular.module('ers-consumer-exampleApp')
  .service('referenceDataService', function ($q, $resource, config, session) {

    function getRefData(valueSetId) {
        var deferred = $q.defer();
        var sessionId = session.getId();

        var headersJson = {};
        headersJson[config.asidHeader] = config.asid;
        headersJson[config.sessionIdHeader] = sessionId;

        var refData = $resource(config.baseUrl + '/v1/ValueSet/' + valueSetId,
            null,
            {get: {method: 'GET', headers: headersJson}}
        );
        refData.get(function(data) {
            deferred.resolve(data);
        }, function() {
            deferred.reject();
        });

        return deferred.promise;
    }

    return {
        getRefData: getRefData
    };
  });
```

## Notes
Consuming application must have a valid session in order to access this endpoint.
