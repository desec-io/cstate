---
title: API and web unreachable via IPv6
date: 2025-11-21 16:30:00
resolved: true
resolvedWhen: 2025-11-22 20:27:00
severity: disrupted
affected:
  - API
  - Website
section: issue
---

deSEC API and web services were inaccessible via IPv6 from Nov 21, 2025, 4:30pm until Nov 22, 2025, 8:27pm UTC.

The issue happened due to an update of the Docker daemon, a piece of software that we use to run several of our components. The new Docker version (although a "minor" upgrade) requires new configuration syntax for IPv6 network bridges. As only the old syntax was in place, IPv6 traffic to web and API services was dropped. Unfortunately, this also included the checkipv6.dedyn.io and update6.dedyn.io endpoints. The issue was resolved by applying the new syntax.

deSEC operates a monitoring system that tests deSEC service quite broadly. However, our API and web services tests did not attempt connecting specifically via IPv4 or IPv6. As IPv4 was working, the monitoring system did not detect this condition. We will amend our test suite to cover this as an additional case.

DNS operations continued throughout (that is, domains hosted at deSEC experienced no outage), including resolution via IPv6.
