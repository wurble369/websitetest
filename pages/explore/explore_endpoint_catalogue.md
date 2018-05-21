---
title: Endpoint Catalogue
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: /explore_endpoint_catalogue.html
summary: "Catalogue of all external e-RS API endpoints"
---

|Id&nbsp;&nbsp;&nbsp;&nbsp;|Name|Family|Verb&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|URI|Status|FHIR|
|---|---|---|---|---|---|
|A001|[Create Professional Session](explore_endpoint_a001.html)|Session|POST|/v1/ProfessionalSession|Live| |
|A002|[Professional Session Select Role](explore_endpoint_a002.html)|Session|PUT|/v1/ProfessionalSession/{sessionKey}|Live| |
|A003|[Delete Professional Session](explore_endpoint_a003.html)|Session|DELETE|/v1/ProfessionalSession/{sessionKey}|Live| |
|A004|[Retrieve Reference Data](explore_endpoint_a004.html)|Reference Data|GET|/v1/ValueSet/{valueSetId}|Live| |
|A005|[Retrieve Referral Request](explore_endpoint_a005.html)|Clinical Referral Information|GET|/v1/ReferralRequest/{id}|Live|[Model](https://data.developer.nhs.uk/specifications/eRS-draftd/Profile.ReferralsForReviewWorklistResponse/ers-referralrequest-1.html)||
|A006|[Retrieve Attachment](explore_endpoint_a006.html)|Clinical ReferralLive| | Information|GET|/v1/Binary/att-{referralRequestAttachmentId|Live| |
|A007|[Retrieve Clinical Information](explore_endpoint_a007.html)|Clinical Referral Information|GET|/v1/Binary/$ers.generateCRI|Live|[Model](https://data.developer.nhs.uk/specifications/eRS-draftd/Profile.ClinicalReferralInformationQuery/ers-clinicalreferralinformation-operation-1.html)|
|A008|[Retrieve Worklist](explore_endpoint_a008.html)|Clinical Referral Information|GET|/v1/ReferralRequest/$ers.fetchworklist|Live|[Model](https://data.developer.nhs.uk/specifications/eRS-draftd/Profile.ReferralsForReviewWorklistQuery/ers-fetchworklist-operation-1.html)|
|A009|[Directory Service Search](explore_endpoint_a009.html)|Service Search|POST|/v1/HealthcareService/$dos.serviceSearch|Alpha| |
|A010|[Patient Service Search](explore_endpoint_a010.html)|Service Search|POST|/v1/HealthcareService/$patient.serviceSearch|Alpha| |
|A011|[Create Referral Request Through Shortlist](explore_endpoint_a011.html)|Referral Request|POST|/v1/CreateReferral|Alpha| |
|A012|[Upload Attachments](explore_endpoint_a012.html)|ReferralAlpha| | Request|POST|/v1/ReferralRequest/{{UBRN}}/$ers.uploadReferralLetter|Alpha| |
|A013|[Accept Referral](explore_endpoint_a013.html)|Referral Request|POST|/v1/ReferralRequest/{{UBRN}}/$ers.accept|Alpha| |
|A014|[Reject Referral](explore_endpoint_a014.html)|Referral Request|POST|/v1/ReferralRequest/{{UBRN}}/$ers.reject|Alpha| |
