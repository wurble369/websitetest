---
title: "BF005: Referral Management"
keywords: business, flow
sidebar: overview_sidebar
toc: false
permalink: /develop_business_flow_bf005.html
summary: "Business flows and their related endpoints"
---

### Definition

This business flow describes the process by which a referring clinician can create a referral with a selection of shortlisted services and all the necessary attributes for it to appear on the referrals for review shortlist (i.e. with a referral letter and a booked appointment). A slot search across all shortlisted services returns the appointment slots that can be booked via e-RS; where appointment slots are not available at the chosen service, the referrer can defer the appointment booking to the provider. The referral letter can be uploaded or amended at any time up a number of days before the appointment, as set by the service (so as to allow enough time for the referral to be reviewed).

While an appointment booking (or a booking deferral) is made at a specific service, referrers are supposed to shortlist more than one service where possible in order to offer patient choice, according to the NHS Choice Framework (item 3).

### This business flow involves the following APIs

* A011 - Create Referral Request Through Shortlist
* A012 - Upload Attachments
* A013 - Accept Referral
* A014 - Reject Referral

### Review the diagram below to learn more

![BF005: Referral Management](images/develop/BF005-ReferralManagement.png)
