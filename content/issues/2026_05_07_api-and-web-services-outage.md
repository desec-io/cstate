---
title: API and web services outage
date: 2026-05-07 04:47:00
resolved: true
resolvedWhen: 2026-05-07 06:47:00
severity: down
affected:
  - API
  - Website
section: issue
---

deSEC API and web services have been unavailable today between 4:47am and 6:47am UTC.

The issue happened due to a scheduled update of our Docker daemon, a piece of software that we use to run several of our components. After the Docker update, one of the Docker containers was not restarted as configured, and as a result, our main web server (which depends on the failing container) also did not start up. All web services (web site, API, and dynDNS update interface) were hence interrupted.

deSEC operates a monitoring system that is supposed to alert our team in case of such events (by escalating through email, text messages, and phone calls within about 10 minutes). The detection of the error condition worked as intended, but the phone alerting was not effective as there was also a mobile network connectivity issue in the area at the same time. We will look into how to increase resilience against such alerting failures.

DNS operations continued throughout (that is, domains hosted at deSEC experienced no outage).
