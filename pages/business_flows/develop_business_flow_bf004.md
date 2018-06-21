---
title: "BF004: Service Search"
keywords: business, flow
sidebar: overview_sidebar
toc: false
permalink: /develop_business_flow_bf004.html
summary: "Business flows and their related endpoints"
---

This business flow describes the process of an authenticated user searching for services. Two options are available:

1. Generic search across the whole directory of services
2. Search aimed at creating a referral for the selected patient.
The second option limits the results to services which the user is able to refer the current patient into, based on the commissioning rules that apply to the user or the patient.

This business flow involves the following APIs:

* A009 - Directory Service Search
* A010 - Patient Service Search

Review the diagram below to learn more:

![BF004: Service Search](images/develop/BF004-ServiceSearch.jpg)
