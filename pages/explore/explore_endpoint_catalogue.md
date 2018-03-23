---
title: Endpoint Catalogue
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: /explore_endpoint_catalogue.html
summary: "Catalogue of all API endpoints"
---

|Id|Name|Family|Verb|URI|
|---|---|---|---|
|A001|[Create Professional Session](/explore_endpoint_a001.html)|Session|POST|[/v1/ProfessionalSession](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/professionalsession/createProfessionalSessionUsingPOST)|
|A002|Professional Session Select Role|Session|PUT|[/v1/ProfessionalSession/{sessionKey}](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/professionalsession/updateProfessionalSessionSelectRoleUsingPUT)|
|A003|Delete Professional Session|Session|DELETE|[/v1/ProfessionalSession/{sessionKey}](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/professionalsession/deleteProfessionalSessionUsingDELETE)|
|A004|Retrieve Reference Data|Reference Data|GET|[/v1/ValueSet/{valueSetId}](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/valueset/getValueSetUsingGET)|
|A005|Retrieve Referral Request|Clinical Referral Information|GET|[/v1/ReferralRequest/{id}](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/referralrequest/getUsingGET)|
|A006|Retrieve Attachment|Clinical Referral Information|GET|[/v1/Binary/att-{referralRequestAttachmentId](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/binary/getAttachmentContentBodyUsingGET)|
|A007|Retrieve Clinical Information|Clinical Referral Information|GET|[/v1/Binary/$ers.generateCRI](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/binary/getClinicalInfoPDFUsingGET)|
|A008|Retrieve Worklist|Clinical Referral Information|GET|[/v1/ReferralRequest/$ers.fetchworklist](http://api-ers.spine2.ncrs.nhs.uk:88/swagger-ui/#!/referralrequest/getWorklistUsingPOST)|
