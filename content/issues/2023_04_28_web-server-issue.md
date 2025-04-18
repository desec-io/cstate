---
title: Web server issue
date: 2023-04-28 04:19:00
resolved: true
resolvedWhen: 2023-04-28 04:33:00
severity: down
affected:
  - API
  - Website
section: issue
---

Today at 04:19am UTC, a Docker container related to Prometheus metrics crashed, which caused nginx to fail. nginx has the unfortunate property to die when a proxy target host is not available. As a result, nginx was stuck in a restart loop and deSEC's web server including the API was unavailable.

At 04:33am UTC, the metrics container was restored, and nginx is running again.
