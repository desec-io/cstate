---
title: DNSSEC Problems due to Replication Issue
date: 2020-06-04 00:00:00
resolved: true
resolvedWhen: 2020-06-04 07:00:00
severity: disrupted
affected:
  - DNS Anycast Frontends
section: issue
---

deSEC DNS operations experienced a partial service disruption. The issue was caused by incomplete replication of zones after their DNSSEC signatures had been renewed, leading to DNSSEC validation failures for certain DNS queries.

# Impact
No data was lost or compromised: our services were not under attack, nor did a physical failure occur.

Signatures on domains that had not been updated since May 28, 2020, were not correctly refreshed. As a consequence, DNSSEC-aware clients or resolvers rejected those expired signatures. Domains whose contents had been updated more recently were provisioned correctly on the frontend DNS servers.

DNS clients or resolvers that do not perform DNSSEC validation were not affected and were able to query all domains at any time.

# Details
You can find [more information in our forum](https://talk.desec.io/t/service-disruption-on-june-4-2020/98).

