---
title: "A006: Retrieve Attachment"
keywords: endpoint, catalogue
sidebar: overview_sidebar
toc: false
permalink: explore_endpoint_a006.html
summary: false
---

## API
[GET /v1/Binary/att-{referralRequestAttachmentId}](https://api.dev1.ers.ncrs.nhs.uk/ers-api/v1/Binary/url)

## Description
This lets users retrieve and download linked files for a referral. Identify the file using both the request and attachment identifier.

## Input
URL.

## Output
To follow.

## Code Sample
Code snippets taken from the consumer example. See [Code Samples](develop_code_samples.html) for further details.

To follow.

## Notes
Get the Attachment identified by the given Referral Request Id and Attachment Id.

### Parameters
| Parameter | Value | Description | Parameter Type | Data Type |
| --------- | ----- | ----------- | -------------- | --------- |
| referralRequestAttachmentId |   | Referral Request Attachment Id | Path | String |

### Response Messages
| HTTP Status Code | Reason |
| ---------------- | ------ |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
