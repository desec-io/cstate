---
title: Delayed replication
date: 2023-02-02 18:15:00
resolved: true
resolvedWhen: 2023-02-02 19:48:00
severity: disrupted
affected:
  - DNS Anycast Frontends
section: issue
---

Due to an internal network issue, new or modified DNS records are currently not being replicated within our network. DNS resolution is not impacted, but frontend machines are serving DNS data from 6:15pm UTC.

This is an internal issue; no attack has occurred. The issue is expected to be resolved around 8pm UTC today.
