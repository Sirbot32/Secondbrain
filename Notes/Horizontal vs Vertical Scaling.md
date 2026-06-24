---
tags: [system-design]
topic: System Design
created: 2026-06-24
status: confirmed
---

# Horizontal vs Vertical Scaling

Vertical scaling means making one machine bigger — adding/upgrading its hardware (CPU, RAM, storage). Horizontal scaling means adding more machines to share the load instead. Vertical scaling hits a hard ceiling: there's a physical limit to how powerful one machine can get, and it's a single point of failure. Horizontal scaling avoids that ceiling because you can just buy more of the same commodity hardware, and it adds redundancy — but it introduces real costs vertical scaling doesn't have, like keeping data consistent across machines (e.g. two servers receiving updates to the same value at the same time, and only one update actually sticking).

Related: [[Load Balancer]]
