---
title: API and web services outage
date: 2020-12-01 05:17:00
resolved: true
resolvedWhen: 2020-12-01 05:36:00
severity: down
affected:
  - API
  - Website
section: issue
---

deSEC API and web services have been unavailable today between 5:17am and 5:36am UTC.

The issue occurred due to the Docker daemon not properly restarting after a scheduled update. All web services (web site, API, and dynDNS update interface) were hence interrupted.

deSEC operates a monitoring system to alert our team in such cases. The system worked properly and alerted us at 5:25am UTC.

DNS operations continued throughout (that is, domains hosted at deSEC experienced no outage).
