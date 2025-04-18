---
title: Ongoing performance issues
date: 2023-01-30 00:00:00
resolved: true
resolvedWhen: 2023-01-30 00:00:00
severity: notice
affected:
  - DNS Anycast Frontends
section: issue
informational: true
---

Since January 20, 2023, our DNS platform service has repeatedly been targeted by DDoS attacks, due to which our servers did not manage to respond to all requests. Attacks usually take around 15 minutes, during which our infrastructure is hit with around 120,000 queries per second.

Over the next couple of days, we will upgrade our infrastructure to handle the increased load spikes. We apologize for any intermittent issues clients may be experiencing until the upgrade is completed. Thank you for your patience!

(Is there any good in it? -- If you will, yes: being targeted for DDoS speaks to the maturity of the platform. It is true for all DNS providers that the day of DoS arrives eventually. We'll do out best to grow beyond it.)
