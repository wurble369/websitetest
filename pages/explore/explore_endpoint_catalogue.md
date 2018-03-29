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
|A001|[Create Professional Session](explore_endpoint_a001.html)|Session|POST|/v1/ProfessionalSession|
|A002|Professional Session Select Role|Session|PUT|/v1/ProfessionalSession/{sessionKey}|
|A003|Delete Professional Session|Session|DELETE|/v1/ProfessionalSession/{sessionKey}|
|A004|Retrieve Reference Data|Reference Data|GET|/v1/ValueSet/{valueSetId}|
|A005|Retrieve Referral Request|Clinical Referral Information|GET|/v1/ReferralRequest/{id}|
|A006|Retrieve Attachment|Clinical Referral Information|GET|/v1/Binary/att-{referralRequestAttachmentId|
|A007|Retrieve Clinical Information|Clinical Referral Information|GET|/v1/Binary/$ers.generateCRI|
|A008|Retrieve Worklist|Clinical Referral Information|GET|/v1/ReferralRequest/$ers.fetchworklist|
|A009|Directory Service Search|???|POST|/v1/HealthcareService/$dos.serviceSearch|
|A010|Patient Service Search|???|POST|/v1/HealthcareService/$patient.serviceSearch|
|A011|Create Referral Request Through Shortlist|???|POST|/v1/CreateReferral|
|A012|Upload Attachments|???|POST|/v1/ReferralRequest/{{UBRN}}/$ers.uploadReferralLetter|
|A013|Accept Referral|???|POST|/v1/ReferralRequest/{{UBRN}}/$ers.accept|
|A014|Reject Referral|???|POST|/v1/ReferralRequest/{{UBRN}}/$ers.reject|
