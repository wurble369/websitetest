---
title: "A007: Retrieve Clinical Information"
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: explore_endpoint_a007.html
summary: false
---

## API
[GET /v1/Binary/$ers.generateCRI](https://api.dev1.ers.ncrs.nhs.uk/ers-api/v1/Binary/$ers.generateCRI?UBRN=UBRN)

## Description
This API lets users create a real-time Portable Document Format (PDF) of the referral. This is suitable for integration into a 3rd party system. You can find the Clinical Information for a referral request using a UBRN.

## Input
UBRN.

## Output
To follow.

## Code Sample
Code snippets taken from the consumer example. See [Code Samples](develop_code_samples.html) for further details.

To follow.

## Notes
Get the Clinical Referral Information for a Referral Request identified by the given UBRN.

### Parameters
| Parameter | Value | Description | Parameter Type | Data Type |
| --------- | ----- | ----------- | -------------- | --------- |
| UBRN |   | UBRN | Query | String |

### Response Messages
| HTTP Status Code | Reason |
| ---------------- | ------ |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
