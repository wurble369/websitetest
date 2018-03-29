---
title: "A005: Retrieve Referral Request"
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: explore_endpoint_a005.html
summary: false
---

## API
[GET /v1/ReferralRequest/{id}](https://api.dev1.ers.ncrs.nhs.uk/ers-api/v1/ReferralRequest/UBRN)

## Description
This API gets the referral request identified by the given ID. For each new referral, the user will be able to get key data attributes. External systems can show these in their system. The user can then see status and content header info.

## Input
UBRN number.

### Example
```javascript
{
 "token": "<token id>"
}
```

### FHIR Structure Definition for Referral Request
```javascript
{
  "resourceType": "ReferralRequest",
  "id": "000234620011",
  "meta": {
    "versionId": "2",
    "profile": [
      "http://fhir.nhs.net/StructureDefinition/ers-referralrequest-1"
    ]
  },
  "contained": [
    {
      "resourceType": "Appointment",
      "id": "appointment",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-appointment-1"
        ]
      },
      "status": "booked",
      "start": "2016-10-10T10:00:00+01:00",
      "end": "2016-10-10T10:00:00+01:00",
      "participant": [
        {
          "actor": {
            "reference": "#300511"
          },
          "status": "accepted"
        },
        {
          "type": [
            {
              "coding": [
                {
                  "system": "http://hl7.org/fhir/ValueSet/encounter-participant-type",
                  "code": "CON"
                }
              ]
            }
          ],
          "actor": {
            "reference": "#123456789012"
          },
          "status": "accepted"
        }
      ]
    },
    {
      "resourceType": "HealthcareService",
      "id": "300511",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-healthcareservice-1"
        ]
      },
      "identifier": [
        {
          "system": "http://fhir.nhs.net/Id/ers-service",
          "value": "300511"
        }
      ],
      "location": {
        "reference": "#RKE123"
      },
      "serviceName": "LGI Orthopaedics Service"
    },
    {
      "resourceType": "Location",
      "id": "RKE123",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-location-1"
        ]
      },
      "identifier": [
        {
          "system": "http://fhir.nhs.net/Id/ods-site-code",
          "value": "RKE123"
        }
      ]
    },
    {
      "resourceType": "Practitioner",
      "id": "123456789012",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-practitioner-1"
        ]
      },
      "identifier": [
        {
          "system": "http://fhir.nhs.net/Id/sds-user-id",
          "value": "123456789012"
        }
      ]
    },
    {
      "resourceType": "Patient",
      "id": "9900002831",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-patient-1"
        ]
      },
      "identifier": [
        {
          "system": "http://fhir.nhs.net/Id/nhs-number",
          "value": "9900002831"
        }
      ]
    },
    {
      "resourceType": "DocumentReference",
      "id": "attachment1",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-documentreference-1"
        ]
      },
      "type": {
        "coding": [
          {
            "system": "http://fhir.nhs.net/ValueSet/ers-attachmenttype-1",
            "code": "REFERRER",
            "display": "Referrer"
          }
        ]
      },
      "indexed": "2016-09-05T14:24:53+01:00",
      "status": "current",
      "description": "Clinical comment as entered by clinician",
      "content": [
        {
          "attachment": {
            "id": "5345434",
            "extension": [
              {
                "url": "http://fhir.nhs.net/StructureDefinition/extension-ers-attachedby-1",
                "valueReference": {
                  "reference": "#123456789012"
                }
              }
            ],
            "contentType": "text/plain",
            "url": "Binary/att-100763-5345434",
            "size": 23000,
            "title": "clinical-comment.txt",
            "creation": "2016-07-04"
          }
        }
      ]
    },
    {
      "resourceType": "DocumentReference",
      "id": "attachment2",
      "meta": {
        "profile": [
          "http://fhir.nhs.net/StructureDefinition/ers-documentreference-1"
        ]
      },
      "type": {
        "coding": [
          {
            "system": "http://fhir.nhs.net/ValueSet/ers-attachmenttype-1",
            "code": "REFERRER",
            "display": "Referrer"
          }
        ]
      },
      "indexed": "2016-09-05T10:24:53+01:00",
      "status": "current",
      "description": "X-ray of relevant body part",
      "content": [
        {
          "attachment": {
            "id": "876220",
            "extension": [
              {
                "url": "http://fhir.nhs.net/StructureDefinition/extension-ers-attachedby-1",
                "valueReference": {
                  "reference": "#123456789012"
                }
              }
            ],
            "contentType": "image/png",
            "url": "Binary/att-100763-876220",
            "size": 20000,
            "title": "animage.png",
            "creation": "2016-07-04"
          }
        }
      ]
    }
  ],
  "extension": [
    {
      "url": "http://fhir.nhs.net/StructureDefinition/extension-ers-appointment-1",
      "valueReference": {
        "reference": "#appointment"
      }
    },
    {
      "url": "http://fhir.nhs.net/StructureDefinition/extension-ers-clinicalinfofirstsubmitted-1",
      "valueDateTime": "2016-07-01T09:00:00Z"
    },
    {
      "url": "http://fhir.nhs.net/StructureDefinition/extension-ers-clinicalinfolastupdated-1",
      "valueDateTime": "2016-07-31T11:20:00Z"
    }
  ],
  "status": "active",
  "specialty": {
    "coding": [
      {
        "system": "http://fhir.nhs.net/ValueSet/ers-specialty-1",
        "code": "DERMATOLOGY",
        "display": "Dermatology"
      }
    ]
  },
  "priority": {
    "coding": [
      {
        "system": "http://fhir.nhs.net/ValueSet/ers-priority-1",
        "code": "ROUTINE",
        "display": "Routine"
      }
    ]
  },
  "patient": {
    "reference": "#9900002831"
  },
  "supportingInformation": [
    {
      "reference": "#attachment1"
    },
    {
      "reference": "#attachment2"
    },
    {
      "reference": "ReferralRequest/000231602100"
    },
    {
      "reference": "ReferralRequest/000231601933"
    }
  ]
}
```

## Output
To follow

## Code Sample
Code snippets taken from the consumer example. See [Code Samples](develop_code_samples.html) for further details.

To follow

## Notes
To follow
